# Yandex Translate Android API
A background task, which lets you use Yandex.Translate API in Android projects easily.
## Requires

* A Yandex API Key - [Sign Up Here](http://api.yandex.com/translate/)

```java
import com.rmtheis.yandtran.language.Language;
import com.rmtheis.yandtran.translate.Translate;

public class test {
    public static void main(String[] args) throws Exception {
        Translate.setKey("[Put your API Key here]");

        String translatedText = Translate.execute("Hola, mundo!", Language.SPANISH, Language.ENGLISH);

        System.out.println(translatedText);
    }
}

```
