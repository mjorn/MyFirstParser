import org.jsoup.Jsoup;
import org.jsoup.nodes.Document;
import org.jsoup.nodes.Element;
import org.jsoup.select.Elements;

import java.io.IOException;

public class Parser {
    public static void main(String[] args) {
        Document doc = null;
        try {

            doc = Jsoup.connect("https://habrahabr.ru/top/").get();

        } catch(IOException e) {
            e.printStackTrace();
            System.out.println("Connecting error: "+e);
        }

        if(doc!=null) {

            System.out.println(doc.title());
            Elements elements = doc.getElementsByAttributeValue("class", "post__title");
            for (Element element : elements) {
                //System.out.println(element);
                Element ahref = element.child(0);
                //System.out.println(ahref);
                String url = ahref.attr("href");
                System.out.println(url);
                String title = ahref.text();
                System.out.println(title);

            }

        }
    }
}
