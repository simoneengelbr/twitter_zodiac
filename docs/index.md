# **<span style="color:#8a7e4a">The cosmic side of Twitter</span>**

Zodiac signs have been around since the 1st millennium before Christ, and they remain in popular culture as identity markers. Many people believe that when a child is brought into this world, their personality and personal relations are shaped by the alignment of 12 constellations on that day. This is described by twelve zodiac signs, split into four elements, each with their own characteristics and compatibilities. 

In the last decade, social media has gained immense power and now plays a major role in many people’s everyday life. More than ever, users of social media feel the need to share different aspects of their lives either by simply sharing a photo or by writing thier personal opinions on a topic for the world to see. **[Twitter](https://twitter.com)** has a large user base of people sharing thoughts and opinions, and following other users who do the same. As a brief overview of the last statistics, there are 340 million accounts on Twitter from which 186 million are daily active. When it comes to how many tweets are sent per day, the number is around **[500 million](https://www.internetlivestats.com/twitter-statistics/)** . If astrology really has an effect on personality and relations, it may be indicated in the writing and followings of people of different zodiac signs on Twitter.

With this idea in mind, we decided to work with Twitter accounts of famous people, as their birthdays are publicly available. With a little help from the Twitter API, information on the most followed accounts were gathered. Profiles belonging to people with Wikipedia pages were loaded together with their followed pages (friends), and their last 50 Tweets before the 20th of November 2020. The birthday of each user was read from their Wikipedia page. The Wikipedia page and birthday is collected to be able to determine the **[zodiac sign](https://askastrology.com/zodiac-signs/)** of every person and also establish to which **[element](https://astrostyle.com/learn-astrology/the-elements-fire-earth-air-and-water-signs/)** the sign belongs.

The result is a dataset with information on famous people's twitter profiles. This data is stored in a dataset compressed in a 82.23MB pickle file. For more detailed information, please visit the **[Data Gathering notebook](https://github.com/simoneengelbr/twitter_zodiac/blob/main/DataGathering.ipynb)**. From this data, we built a network of the famous twitter users connected by who follows who. In this study, we analyzed the network of users and the tweets of each user to search for unique attributes among users with different zodiac signs. This analysis is detailed in the **[Explainer notebook](https://github.com/simoneengelbr/twitter_zodiac/blob/main/Zodiac.ipynb)** .

# **<span style="color:#8a7e4a">What does the network look like?</span>**

Before starting an in depth analysis, it's a good idea to first see what the network looks like. A total number of 2037 nodes and 124721 links constitute our network. Each node represents a Twitter user, colored by zodiac sign, and each link represents how users are connected by follows. In other words, this networks shows who is following who. Notice that some of the nodes are bigger than the others, this is because some people follow a lot of other people, like Barack Obama(598K), and some of them do not follow that many at all, like Cristiano Ronaldo(52). There are even cases when a personality does not follow anyone back, which is the case for Taylor Swift, Eminem, Adele, and more.
 
<p align="center">
  <img width="1200" height="950"  src="https://raw.githubusercontent.com/simoneengelbr/twitter_zodiac/main/docs/TransparentNetwork.png?">
</p>

The in-out degree distribution graph is way of illustrating how the people in the network interact. The in-degree can be interpreted as the popularity of the personality among the other users of the platform and the out-degree the interest that a specific user has in another accounts. Usually we tend to follow the accounts that we find interesting. 

<p align="center">
  <img width="1200" height="450" src="https://raw.githubusercontent.com/simoneengelbr/twitter_zodiac/main/docs/TransparentInOutDegreeDistribution.png?">
</p>

In the graph above, it can be seen that many users follow few or no other users in the network, but there are a few users that follow houndreds of others. In regards to followers, most people have less than 100 people in the network following them. This dynamic is typical for social networks.

# **<span style="color:#8a7e4a">Content analysis</span>**

When it comes to use of language, in the social media area it is very personal. This is because when someone writes on the internet, that person is often directly stating their opinion. Taking into consideration the astology factor, it is assumed that some zodiac signs tend to be more sensible, some more harsh, while others don't even want to share what they truly think with other people. However, this does not entirely apply to public figures as for some of them, their personal account is being managed by their PR-manager or CM. 

The following wordclouds display words most uniquely tweeted by each zodiac sign. To be able to accomplish this, words are extracted from the tweets of the users and analyzed with a method called term frequency–inverse document frequency (TF-IDF). 

![ZodiacSigns](ZodiacSigns.png)

The resulting word clouds show words that are more especially used by users in each zodiac sign. The word clouds are not obviously meaningful, but this could in part be due to the very broad content on Twitter. In that regard, the dataset of tweets is not particularly large, and unusual topics will stand out. 

# **<span style="color:#8a7e4a">Communities</span>**

So far, the analysis has focused on zodiac signs as a way to create different groups to analyze in the network. However, this is not a proper scientific analysis, as they can be interpreted as arbitrary partitions. To find the real communities in the network, the a method known as the Louvain Algorithm is used.


<p align="center">
  <img width="1200" height="450" src="https://raw.githubusercontent.com/simoneengelbr/twitter_zodiac/main/docs/TransparentCommunityDistribution.png?">
</p>


As mentioned, it is a common belief in astrology that some signs tend to be more compatible with others. If this were true, there may be a strong presence of compatible signs within communities. To check this, the zodiac distribution for each community is plotted in the graphs below.

<p align="center">
  <img width="1200" height="1400" src="https://raw.githubusercontent.com/simoneengelbr/twitter_zodiac/main/docs/TransparentZodiacDistributionCommunities.png?">
</p>

These graphs show a somewhat even spread in zodiac signs within communities, to the point that there are no significant compatabilities indicated.

However, the signs can be grouped into 4 elements. Astrology claims that signs within the same element are compatible, and each element has an opposite, compatible element. If this were true, finding the compatibility in the elements should be easier, as there are less combinations to compare. To check this, the element distribution inside each community is plotted. 

<p align="center">
  <img width="1200" height="1400" src="https://raw.githubusercontent.com/simoneengelbr/twitter_zodiac/main/docs/TransparentElementDistributionCommunity.png?">
</p>

Here, the even distribution is even more apparent. Thus, astrologic signs have no apparent influence on community formation.

# **<span style="color:#8a7e4a">Sentiment of the communities</span>**
Sentiment analysis is a method of analyzing the tone of words. According to astrology, some signs tend to be more positive than others. If we perform a sentiment analysis on the tweets of the users in the network, we may be able to see differences between the zodiac signs.

To analyze the sentiment the dataset **[AFINN](https://github.com/fnielsen/afinn)** was used. It was developed specifically to analyse tweets, as tweets include slang terms like 'lol'. This dataset rates words with a positive or negative value based on their sentiment.

Below is an analysis of the average sentiment (with a confidence interval determined from the standard deviation) of users in each zodiac sign. The plot shows little variation between zodiac signs, and indicates no significant difference between signs.
<p align="center">
  <img width="1200" height="450" src="https://raw.githubusercontent.com/simoneengelbr/twitter_zodiac/main/docs/TransparentAverageSentimentZodiac.png?">
</p>

If we instead calculate average sentiment within communities, there is a much bigger difference:
<p align="center">
  <img width="1200" height="450" src="https://raw.githubusercontent.com/simoneengelbr/twitter_zodiac/main/docs/Transparent.png?">
</p>

Both the signs and the communities use positive words in their tweets. This could be interpreted that, as most of the users in the network are public figures, usually they use their Twitter accounts to promote their content and therefore tweet words with more positive sentiment.

Throughout the analysis, no significant differences have been found between users of different zodiac signs, despite tackling the data from different angles. Therefore, based on the data of over 2000 popular users on twitter, we cannot determine that astrology has an influence on people in regards to personality or compatibility.
