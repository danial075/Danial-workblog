---
layout: default
---
[homepage](/index)

<p> Over the summer I took part in a mentorship program. The task was to keep developing and incrementally enhancing the same application over several weeks. I chose to make a trading program which takes in a stock’s name, price and ticker and parses it in via a text file. The user selects if they want to buy or sell the stock and the quantity.</p>

![Trading Program, output](https://danial075.github.io/Users/danialsheikh/Documents/Github/danial075.github.io/console33.png)

<p>The innovations I made to it were using a JSON file instead of plain text which led me to installing Maven on my machine and making use of a JSON library called GSON parser. </p>

```java
try {
			Reader reader = new FileReader(
					"/Users/danialsheikh/Desktop/Stocks.json");
			Gson g = new Gson(); // This is used as a parser
			App[] stocks = g.fromJson(reader, App[].class); // On the LHS new array of type stocks and on the rhs
															// using the parser and fromJson method which allows
															// us to read the jsonfile in an array format
			for (App i : stocks) {
				names.add(i.getStock_Name());
				tickers.add(i.getStock_Ticker());
				prices.add(i.getStock_Price());
			}
```

<p>Then I created a GUI Login (using the swing library) which allows the user to enter a username and password to confirm their credentials. I then implemented a REST API using Springboot which allows me to publish the API and deploy it on the cloud. I really enjoyed this project as I had created from scratch, and it was really satisfying to track my progress from the start to finish and making use of frameworks widely used in the software and finance industry.</p>

![Trading Program, output](/Users/danialsheikh/Documents/Github/danial075.github.io/login.png)

```java
package com.example.tradingprogramrest;

import org.springframework.boot.SpringApplication;
import org.springframework.boot.autoconfigure.SpringBootApplication;

@SpringBootApplication
public class TradingprogramRestApplication {

	public static void main(String[] args) {
		SpringApplication.run(TradingprogramRestApplication.class, args);
	}

}

```
