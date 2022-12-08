package seleniumpackage;
import java.util.ArrayList;
import java.util.Set;
import java.util.concurrent.TimeUnit;
import org.openqa.selenium.By;
import org.openqa.selenium.JavascriptExecutor;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.chrome.ChromeDriver;
import org.openqa.selenium.interactions.Actions;
import io.github.bonigarcia.wdm.WebDriverManager;

public class AnsumanPattnaikWaffer {
public static void main(String[] args) throws InterruptedException {
	//*open chrome driver*//
WebDriverManager.chromedriver().setup();
WebDriver driver =new ChromeDriver();
//*Maximize the window*//
driver.manage().window().maximize();
//*Implicity wait*//
driver.manage().timeouts().implicitlyWait(10,TimeUnit.SECONDS);
//*Opening the URL*//
driver.get("https://docs.google.com/forms/d/e/1FAIpQLSeksbTPgj20M1lefvkxUTrG5EAkFoRqyKHdfg3kI2j6cLLLdw/viewform?usp=sf_link");
//*First name field*//
WebElement W=driver.findElement(By.xpath("(//div[@class='ndJi5d snByac'])"));
Actions act = new Actions(driver);
act.click(W).perform();
//*Enter input*//
driver.findElement(By.xpath("(//div[@class='ndJi5d snByac'])")).sendKeys("Ansuman Pattnaik");
//*Scroll option*//
JavascriptExecutor js=(JavascriptExecutor)driver;
for(int i=0;i<=2;i++) {
	Thread.sleep(1000);
	js.executeScript("window.scrollBy(0,100)");}
//*mail id  field*//
WebElement W1=driver.findElement(By.xpath("(//div[@class='whsOnd zHQkBf'])"));
Actions act1 = new Actions(driver);
act1.click(W1).perform();
W1.sendKeys("mail@mail.com");
//*Drop down option*//
JavascriptExecutor js1=(JavascriptExecutor)driver;
for(int i=0;i<=2;i++) {
	Thread.sleep(1000);
	js1.executeScript("window.scrollBy(0,100)");}
//*Scroll selection option*//
driver.findElement(By.xpath("//div[@class='rq8Mwb']")).click();
JavascriptExecutor js2=(JavascriptExecutor)driver;
for(int i=0;i<=2;i++) {
	Thread.sleep(1000);
	js2.executeScript("window.scrollBy(0,100)");}
//*Resume section*//
driver.findElement(By.xpath("//div[@class='edhGSc zKHdkd kRy7qc RdH0ib yqQS1']")).click();
driver.findElement(By.xpath("//div[@class='edhGSc zKHdkd kRy7qc RdH0ib yqQS1']")).sendKeys("C:/Users/91768/Desktop");
//*Total experience*//
driver.findElement(By.xpath("//div[@class='MocG8c HZ3kWc mhLiyf LMgvRb KKjvXb DEh1R']")).click();
JavascriptExecutor js3=(JavascriptExecutor)driver;
for(int i=0;i<=2;i++) {
	Thread.sleep(1000);
	js3.executeScript("window.scrollBy(0,100)");}
 //*Submit button*//
driver.findElement(By.xpath("//div[@class='NPEfkd RveJvd snByac']")).click();
//*Clear form button*//
driver.findElement(By.xpath("//div[@class='uArJ5e UQuaGc kCyAyd l3F1ye TFBnVe M9Bg4d']")).click();
//*Closing the browser*//
driver.close();
}
}
