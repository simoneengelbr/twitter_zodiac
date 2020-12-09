# **<span style="color:#8a7e4a">What can we learn from social media?</span>**
  
Living in a decade in which technology gained the power, social media started to play a major role in every people's life. Facebook, Instagram or Twitter are just few of the names of the platforms that have a daily increase in the number of the new accouns created. This highlights the fact that people feel more and more the need to share different aspects of their lifes either by simply sharing a photo or thier personal opinions related to a topic. With this idea in mind, we decided to work with the most followed **[Twitter](https://twitter.com)** accounts of famous people. As a brief overview of the last statistics, there are 340 million accounts on Twitter from which 186 million are daily active. When it comes to how many tweets are sent per day, the number is around 500 million.  

With a little help from the Twitter API, the most followed accounts of famous people together with their handle, number of following accounts, and their last 50 Tweets from the past week (16/11/2020 - 20/11/2020) were been collected. Wikipedia API was also used to extract the birthday of those famous people. These actions have been done to be able to determine the **[zodiac sign](https://askastrology.com/zodiac-signs/)** of every person and also establish to which **[element](https://astrostyle.com/learn-astrology/the-elements-fire-earth-air-and-water-signs/)** does that sign belongs. This information is compressed in a 82.23MB pickle file. For more detailed information, please visit the Explainer Notebook. 

# **<span style="color:#8a7e4a">How does the network looks like?</span>**

Before starting analysing in depth, a good idea is to first see how the network looks like. A total number of 2037 nodes and 124721 links constitutes the network. Each node represents a personality's zodiac sign and each link represents how they are connected. In other words, this networks shows who is following who. It can be noticed that some of the nodes are bigger than the other ones and this is because some of the people follow a lot of other people: Barack Obama(598K) and some of them do not follow that many people: Cristiano Ronaldo(52). There are also cases when a personality does not follow anyone back: Taylor Swift, Eminem, Adele.
 
<p align="center">
  <img width="1200" height="950"  src="https://raw.githubusercontent.com/simoneengelbr/twitter_zodiac/main/docs/TransparentNetwork.png?token=AK2UC2M5B4KT5JPRRZZXPNS73IIAU">
</p>

The in-out degree distribution graph is another way of showing how people interact with each other. In-degree can be interpreted as the popularity of the personality among the other users of the platform and the out-degree the interest that a specific user has in another accounts. Usually we tend to follow the accounts that we find interesting. 

<p align="center">
  <img width="1200" height="450" src="https://raw.githubusercontent.com/simoneengelbr/twitter_zodiac/main/docs/TransparentInOutDegreeDistribution.png?token=AK2UC2LNLJB2HSDV3TER74273IKWO">
</p>

# **<span style="color:#8a7e4a">Content analysis</span>**

When it comes to the language used, in the social media area it is very personal. This is because when someone writes on the internet, that person is actually stating his opinion. Taking into consideration the astology factor, it is already known that some zodiac signs tend to be more sensible, other ones more harsh and others do not even want to share what they truly think with other people. To get a better understanding 
 
![ElementWater](ElementWater.png)
![ElementEarth](ElementEarth.png)
![ElementFire](ElementFire.png)
![ElementAir](ElementAir.png)


# **<span style="color:#8a7e4a">Communities</span>**

<p align="center">
  <img width="1200" height="450" src="https://raw.githubusercontent.com/simoneengelbr/twitter_zodiac/main/docs/TransparentCommunityDistribution.png?token=AK2UC2PVGJD7FV5OOKLEZGK73ILSO">
</p>

<p align="center">
  <img width="1200" height="1400" src="https://raw.githubusercontent.com/simoneengelbr/twitter_zodiac/main/docs/TransparentZodiacDistributionCommunities.png?token=AK2UC2LQVP4G5ZCLLN4OXXC73IG4E">
</p>

<p align="center">
  <img width="1200" height="1400" src="https://raw.githubusercontent.com/simoneengelbr/twitter_zodiac/main/docs/TransparentElementDistributionCommunity.png?token=AK2UC2LK2PCHVZWQXWGW6SK73ILQM">
</p>

# **<span style="color:#8a7e4a">Sentiment of the communities</span>**
<p align="center">
  <img width="1200" height="450" src="https://raw.githubusercontent.com/simoneengelbr/twitter_zodiac/main/docs/TransparentAverageSentimentZodiac.png?token=AK2UC2IE3OH2BIJ7CMVAR7C73IKCA">
</p>


<p align="center">
  <img width="1200" height="450" src="https://raw.githubusercontent.com/simoneengelbr/twitter_zodiac/main/docs/Transparent.png?token=AK2UC2MSNPSAO5Q6ECCDW2K73IDYU">
</p>



