# Add a data driven scenario of adding book feature

To see how Cucumber run feature which is data driven, we are going to add one scenario in "buy_book.feature" under "features" folder.

`cd features`

![alt text](https://raw.githubusercontent.com/hy1984427/BDD-with-PageObject/master/images/ChangeFolderToFeatures.png "Change folder to features")

Then we need to add following content to it.

<pre><code>Scenario Outline: Consumer can add a book to shopping cart
    Given I open "http://www.amazon.com/"
    When I search for "<book>"
    And I open the first book
	And I add the first book to shopping cart
	Then I should see the book in my shopping cart
	Examples:
	| book             |
	| The Lean Startup |
	| Steve Jobs       |
</pre></code>

![alt text](https://raw.githubusercontent.com/hy1984427/BDD-with-PageObject/master/images/BuyBookDataDrivenFeatureFile.png "Add data driven scenario into buy_book.feature")
