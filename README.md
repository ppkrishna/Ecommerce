# Ecommerce
End-to-End Shopping Website Transaction

package seleniumpackage;

import org.openqa.selenium.By;
import org.openqa.selenium.WebDriver;

import org.openqa.selenium.chrome.ChromeDriver;

public class Seleniumclass {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		
		//System.setProperty("webdriver.http.factory", "apache");
		

	//System.setProperty("webdriver.chrome.driver", "C:\\Users\\prateek.krishna.INCOFORGETECH\\Documents\\Automation\\selenium\\chromedriver_win32\\chromedriver.exe");
	System.setProperty("webdriver.chrome.driver", "C:/Users/prateek.krishna.INCOFORGETECH/Documents/Automation/selenium/chromedriver_win32/chromedriver.exe");	
		
	//Create driver object for chrome browser
		//Class name = ChromeDriver
		WebDriver driver = new ChromeDriver();
		 
		//Implement the method of web drive
		 
		//Go to the url
		 driver.get("https://www.saucedemo.com/");
		 
		 driver.manage().window().maximize();
		 
		 driver.findElement(By.id("user-name")).sendKeys("standard_user");
		 driver.findElement(By.id("password")).sendKeys("secret_sauce");
		 driver.findElement(By.id("login-button")).click();
		 	driver.findElement(By.partialLinkText("Sauce Labs Bike Light")).click();
		 	
//driver.findElements(By.xpath("//*[@class='btn_primary btn_inventory']"));

//driver.findElement(By.xpath("*[contains(@button,'btn_primary btn_inventory')]")).click();;
		 	
		 	
		 driver.findElement(By.xpath("//button[@class='btn_primary btn_inventory']")).click();
		 
		 
	
		 	driver.findElement(By.xpath("//span[@class='fa-layers-counter shopping_cart_badge']")).click();
		 	driver.findElement(By.linkText("CHECKOUT")).click();
		 	
		 	driver.findElement(By.id("first-name")).sendKeys("Prateek");
		 	driver.findElement(By.id("last-name")).sendKeys("Krishna");
		 	driver.findElement(By.id("postal-code")).sendKeys("110091");
		 	
		 	driver.findElement(By.xpath("//input[@class=\"btn_primary cart_button\"]")).click();
		 	
		 	driver.findElement(By.linkText("FINISH")).click();
		 	
		 	driver.close();
		 	
		 	
		 //Get the title and print it
		 System.out.println(driver.getTitle());
		 

	}

}
