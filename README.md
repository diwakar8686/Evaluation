# Evaluation

package Evaluation;

import javax.swing.JList;

import org.apache.commons.compress.harmony.pack200.IntList;
import org.openqa.selenium.WebDriver;
import org.openqa.selenium.WebElement;
import org.openqa.selenium.chrome.ChromeDriver;
import org.testng.Assert;
import org.testng.annotations.AfterClass;
import org.testng.annotations.BeforeClass;
import org.testng.annotations.Test;

import io.github.bonigarcia.wdm.WebDriverManager;

pu<blic class HomeKitchenPage {
	
	public WebDriver driver;
	
	@BeforeClass
	public void setup() {
		WebDriverManager.chromedriver().setup();
		driver= new ChromeDriver();
		driver.manage().window().maximize();
		driver.get("https://www.naaptol.com/");
		
		
	}
	 @AfterClass
	 public void tearDown() {
		 driver.quit();
	 }
	 
	 public class BaseTest extends HomeKitchenPage{
		 @Test
		public void testApplyPriceFilter() {
			 BaseTest page = new BaseTest();
			 page.clickBaseTestCategory();
			 page.testApplyPriceFilter();
			 
		 }
		 @Test
		public void testProductTitlesAreDisplayed() {
			 HomeKitchenPage page = new HomeKitchenPage();
			 page.clickHomeKitchenCategory();
			  list<WebElement> titles = page.getProductTitles();
			  Assert.assertTrue(titles.size()>0);
		 }

		 private void clickBaseTestCategory() {
			// TODO Auto-generated method stub
			
		 }
		 
	 }

	 @Test
	public void clickHomeKitchenCategory() {
		// TODO Auto-generated method stub
		
	 }
	 @Test
	public list<WebElement> getProductTitles() {
		// TODO Auto-generated method stub
		return null;
	 }
	 

}

![image](https://github.com/user-attachments/assets/cb459aa3-937f-4a10-b3eb-40599d69c4ab)
