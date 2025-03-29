# RightNets: A Dataset About Social Media Activity During the 2024 European Elections in Italy

The [RightNets](https://rightnets.unimc.it/) dataset provides a corpus of social media activity in the months leading up to the 2024 European elections in Italy. It includes 10,000 tweets and 411 Facebook posts. The data was collected using automated web scraping tools provided by [Apify](https://apify.com/), specifically the [Facebook Hashtag Scraper](https://apify.com/apify/facebook-hashtag-scraper)  and the [Tweet Scraper V2](https://apify.com/apidojo/tweet-scraper).
- For Facebook data, we identified posts by targeting specific hashtags relevant to the 2024 European elections: “UsaIlTuoVoto” , “europee2024”, “elezioni2024”, “elezionieuropee2024”, and “elezionieuropee”. Posts containing at least one of these hashtags were retrieved without setting a limit on the number of posts or imposing a time frame on their creation dates.
- For X, the data collection process focused on tweets containing at least one of the same set of keywords, but with additional restrictions: only tweets created within the six months preceding the 2024 European elections—between January 1, 2024, and June 10, 2024—were considered. The dataset was further limited to the first 10,000 results matching these criteria.

## Data Description

The main data directory is “italian-eu-2024-posts” which contains to sub-directories, one for the Facebook posts and the other for the X posts. 

	italian-eu-2024-posts
	 ├─ facebook
	 │  └─ data.csv
	 ├─ x
	 │  └─ data.csv
	 └─ keywords.txt
		  
The following files are available
- [italian-eu-2024-posts/facebook/data.csv](italian-eu-2024-posts/facebook/data.csv): Contains the Facebook dataset with columns representing post metadata (e.g., postId, URL, text), engagement statistics (e.g., likesCount, sharesCount, commentsCount), and posting date.
- [italian-eu-2024-posts/x/data.csv](italian-eu-2024-posts/x/data.csv): Contains the Twitter dataset, including columns for tweet metadata (e.g., id, URL), engagement statistics (e.g., retweetCount, replyCount, likeCount, quoteCount), and creation timestamp.
- [italian-eu-2024-posts/keywords.txt](italian-eu-2024-posts/keywords.txt): A file listing the keywords used to identify and filter relevant posts and tweets, reflecting a focus on election-related topics, candidates, and campaign themes.

The following table describes the fields available in the Facebook and X CSV files, along with each field data type.
| **Facebook**         |                                        | **X**               |                                       |
|----------------------|----------------------------------------|---------------------|---------------------------------------|
| **Field**            | **Data Type**                          | **Field**           | **Data Type**                         |
|     postId           |     String                             |     id              |     String                            |
|     likesCount       |     Unsigned integer                   |     retweetCount    |     Unsigned integer                  |
|     sharesCount      |     Unsigned integer                   |     replyCount      |     Unsigned integer                  |
|     commentsCount    |     Unsigned integer                   |     likeCount       |     Unsigned integer                  |
|     date             |     Date (YYYY-MM-DDThh:mm:ss.sssZ)    |     quoteCount      |     Unsigned integer                  |
|                      |                                        |     createdAt       |     Date (ddd mmm DD hh:mm:ss TZD)    |
|                      |                                        |     isRetweet       |     Boolean (true/false)              |
|                      |                                        |     isReply         |     Boolean (true/false)              |
|                      |                                        |     isQuote         |     Boolean (true/false)              |


## Dataset Release Agreement

The dataset is freely released for research and educational purposes. Please cite as
- P. Sernani, Social media and electoral dynamics: A dataset of X and facebook activity during the 2024 European elections, Data in Brief 59 (2025). doi:10.1016/j.dib.2025.111407.
	 
Bibtex entry:

	@article{Sernani2025,
	  author	= {Paolo Sernani},
	  title		= {Social media and electoral dynamics: A dataset of X and facebook activity during the 2024 European elections},
	  journal	= {Data in Brief},
	  volume	= {59},
	  pages		= {111407},
	  year		= {2025},
	  doi		= {10.1016/j.dib.2025.111407},
	}

The paper is open access and available here <https://www.sciencedirect.com/science/article/pii/S2352340925001398>.

## Acknowledgement

This dataset was produced within the framework of the project ‘Normative and Digital Solutions to Counter Threats during National Election Campaigns - RightNets’, funded by the European Union - Next Generation EU under the Prin 2022 PNRR call, Mission 4, Component 2, Investment 1.1, P2022MCYCK, CUP D53D23022340001. Views and opinions expressed are however those of the author(s) only and do not necessarily reflect those of the European Union or the European Commission. Neither the European Union nor the European Commission can be held responsible for them.

---

<p align="center">
	<img src="images/signature.png" alt="PRIN logos">
</p>