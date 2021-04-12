import org.junit.jupiter.api.Assertions;
import org.junit.jupiter.api.Test;
import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.chrome.ChromeDriver;

import java.util.concurrent.TimeUnit;

public class MyFirstAutoTest {

    public static WebDriver driver;
@Test
    public void login () throws InterruptedException {
        System.setProperty("webdriver.chrome.driver", "D:\\ChromeDriver\\chromedriver.exe");
        driver= new ChromeDriver();
        driver.manage().window().maximize();
        driver.manage().timeouts().implicitlyWait(30, TimeUnit.SECONDS);
driver.get("http://users.bugred.ru/user/login/index.html");
driver.findElement(By.xpath("//input[@name='login']")).sendKeys("autotest12@gmail.com");
    driver.findElement(By.name("password")).sendKeys("autotest");
    driver.findElement(By.xpath("/html/body/div[3]/div[1]/div[1]/form/table/tbody/tr[3]/td[2]/input")).click();
    WebElement qa = driver.findElement(By.xpath("//a[contains(text(),'Добавить пользователя')]"));
    Assertions.assertEquals(true, qa.isDisplayed());
    driver.findElement(By.xpath("//tbody/tr[4]/td[1]/input[1]")).sendKeys("autotesterr");
    driver.findElement(By.xpath("//button[contains(text(),'Найти')]")).click();
    driver.findElement(By.xpath("//a[contains(text(),'Добавить пользователя')]")).click();
    driver.findElement(By.xpath("//tbody/tr[1]/td[2]/input[1]")).sendKeys("HWautotest123");
    driver.findElement(By.xpath("//tbody/tr[2]/td[2]/input[1]")).sendKeys("autotester123@gmail.com");
    driver.findElement(By.xpath("//tbody/tr[3]/td[2]/input[1]")).sendKeys("111");
    driver.findElement(By.xpath("//tbody/tr[21]/td[2]/input[1]")).click();
    driver.findElement(By.xpath("//*[@id=\"fat-menu\"]/a")).click();
    driver.findElement(By.xpath("//*[@id=\"fat-menu\"]/ul/li[1]/a")).click();
    driver.findElement(By.xpath("//tbody/tr[2]/td[2]/input[1]")).clear();
    driver.findElement(By.xpath("//tbody/tr[2]/td[2]/input[1]")).sendKeys("hwautotest");
    driver.findElement(By.xpath("//tbody/tr[3]/td[2]/select[1]")).click();
    driver.findElement(By.xpath("//option[contains(text(),'Мужской')]")).click();
    driver.findElement(By.xpath("//tbody/tr[4]/td[2]/input[1]")).click();
    driver.findElement(By.xpath("//tbody/tr[4]/td[2]/input[1]")).sendKeys("01012000");
    driver.findElement(By.xpath("//tbody/tr[5]/td[2]/input[1]")).click();
    driver.findElement(By.xpath("//tbody/tr[5]/td[2]/input[1]")).sendKeys("01012000");
    driver.findElement(By.xpath("//tbody/tr[6]/td[2]/textarea[1]")).clear();
    driver.findElement(By.xpath("//tbody/tr[6]/td[2]/textarea[1]")).sendKeys("тестировать");
    driver.findElement(By.xpath("//tbody/tr[7]/td[2]/input[1]")).sendKeys("000000000000");
    driver.findElement(By.xpath("//tbody/tr[8]/td[2]/input[1]")).click();
}

}
