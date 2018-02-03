# Business-Scenario-using-CucumberBDD
Login.feature , stepImplementations, CucumberTestRuner and Results

#Each feature contains one feature
#Feature files use Gherkin language - business language
Feature: Testing the page functionality of UENI Websites

  #A feature may have given different specific scenarios
  #Scenarios use Given - When - Then structure
  Scenario: Testing the UENI Web pages and book for services
  
    Given Dani's Barber Shop browser/UENI
    When I click on enter button
    Then I navigate to the web pages
    And Book for services
    
    Given RiverKwaiMassage browser/UENI
    When I click on enter button
    Then I navigate to the web pages
    And Book services
    
    Given AS GLAS browser/UENI
    When I click on enter button
    Then I navigate to the web pages
    And I cannot automatically book for services
    
    
    
    stepImplemen tations
    
    package stepImplementations;

import cucumber.api.java.en.Given;
import cucumber.api.java.en.Then;
import cucumber.api.java.en.When;

public class BDDLoginTest {
	
	@Given("^Dani's Barber Shop browser/UENI$")
	public void Dani_s_Barber_Shop_browser_UENI(){
	System.out.println("Dani's Barber Shop browser/UENI");   
	
	}

	@When("^I click on enter button$")
	public void I_click_on_enter_button(){
	System.out.println("I click on enter button");
	 
	}

	@Then("^I navigate to the web pages$")
	public void I_navigate_to_the_web_pages(){
	System.out.println("I navigate to the web pages");
	    
	}

	@Then("^Book for services$")
	public void Book_for_services(){
    System.out.println("Book for services");
	   
	}

	@Given("^RiverKwaiMassage browser/UENI$")
	public void Riverkwaimassage_browser_UENI(){
    System.out.println("Riverkwaimassage browser/UENI");
	   
	}

	@Then("^Book services$")
	public void book_services(){
    System.out.println("Book services");
	 
	}

	@Given("^AS GLAS browser/UENI$")
	public void AS_GLAS_browser_UENI(){
	System.out.println("AS GLAS browser/UENI");
	   
	}

	@Then("^I cannot automatically book for services$")
	public void I_cannot_automatically_book_for_services(){
	System.out.println("I cannot automatically book for services");   
	
	}
}


CucumberTestRunner

package CucumberTest;

import org.junit.runner.RunWith;

import cucumber.api.CucumberOptions;
import cucumber.api.junit.Cucumber;

@RunWith(Cucumber.class)
@CucumberOptions(
		      features = "Features", glue = {"stepImplementations"}  
		)
public class CucumberTestRunner {

}


Results


#Each feature contains one feature
#Feature files use Gherkin language - business language
Feature: Testing the page functionality of UENI Websites
Dani's Barber Shop browser/UENI
I click on enter button
I navigate to the web pages
Book for services
Riverkwaimassage browser/UENI
I click on enter button
I navigate to the web pages
Book services
AS GLAS browser/UENI
I click on enter button
I navigate to the web pages
I cannot automatically book for services

  #A feature may have given different specific scenarios
  #Scenarios use Given - When - Then structure
  Scenario: Testing the UENI Web pages and book for services # features/Login.feature:7
    Given Dani's Barber Shop browser/UENI                    # BDDLoginTest.Dani_s_Barber_Shop_browser_UENI()
    When I click on enter button                             # BDDLoginTest.I_click_on_enter_button()
    Then I navigate to the web pages                         # BDDLoginTest.I_navigate_to_the_web_pages()
    And Book for services                                    # BDDLoginTest.Book_for_services()
    Given RiverKwaiMassage browser/UENI                      # BDDLoginTest.Riverkwaimassage_browser_UENI()
    When I click on enter button                             # BDDLoginTest.I_click_on_enter_button()
    Then I navigate to the web pages                         # BDDLoginTest.I_navigate_to_the_web_pages()
    And Book services                                        # BDDLoginTest.book_services()
    Given AS GLAS browser/UENI                               # BDDLoginTest.AS_GLAS_browser_UENI()
    When I click on enter button                             # BDDLoginTest.I_click_on_enter_button()
    Then I navigate to the web pages                         # BDDLoginTest.I_navigate_to_the_web_pages()
    And I cannot automatically book for services             # BDDLoginTest.I_cannot_automatically_book_for_services()

1 Scenarios (1 passed)
12 Steps (12 passed)
0m0.199s
