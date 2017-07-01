# Yandex Translate Android API
A background task, which lets you use Yandex.Translate API in Android projects easily.
## Requires

* A Yandex API Key - [Sign Up Here](http://api.yandex.com/translate/)


Quickstart
==========
- In TranslatorBackgroundTask.java put your API key in `String yandexKey = "YOUR_API_KEY";`
- Below is a MainActivity.java file which executes the Yandex Translate Background Task
```java
import co.oriens.yandex_translate_android_api.TranslatorBackgroundTask;
import android.util.Log;

public class MainActivity extends Activity{
    //Set context
    Context context=this;
    
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        
        //Default variables for translation
        String textToBeTranslated = "Hello world, yeah I know it is stereotye.";
        String languagePair = "en-fr"; //English to French ("<source_language>-<target_language>")
        //Executing the translation function
        Translate(textToBeTranslated,languagePair);
    }
    
    //Function for calling executing the Translator Background Task
    void Translate(String textToBeTranslated,String languagePair){
        TranslatorBackgroundTask translatorBackgroundTask= new TranslatorBackgroundTask(context);
        String translationResult = translatorBackgroundTask.execute(textToBeTranslated,languagePair); // Returns the translated text as a String
        Log.d("Translation Result",translationResult); // Logs the result in Android Monitor
    }
}

```
