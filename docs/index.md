# **<span style="color:#8a7e4a">The cosmic side of Twitter</span>**

Zodiac signs have been around since the 1st millennium before Christ, and they remain in popular culture as identity markers. Many people believe that when a child is brought into this world, their personality and personal relations are shaped by the alignment of 12 constellations on that day. This is described by twelve zodiac signs, split into four elements, each with their own characteristics and compatibilities. 

In the last decade, social media has gained immense power and now plays a major role in many people’s everyday life. More than ever, users of social media feel the need to share different aspects of their lives either by simply sharing a photo or by writing thier personal opinions on a topic for the world to see.

**[Twitter](https://twitter.com)** has a large user base of people sharing thoughts and opinions, and following other users who do the same. As a brief overview of the last statistics, there are 340 million accounts on Twitter from which 186 million are daily active. When it comes to how many tweets are sent per day, the number is around **[500 million](https://www.internetlivestats.com/twitter-statistics/)** . If astrology really has an effect on personality and relations, it may be indicated in the writing and followings of people of different zodiac signs on Twitter.

With this idea in mind, we decided to work with Twitter accounts of famous people, as their birthdays are publicly available. With a little help from the Twitter API, information on the most followed accounts were gathered. Profiles belonging to people with Wikipedia pages were loaded together with their followed pages (friends), and their last 50 Tweets before the 20th of November 2020. The birthday of each user was read from their Wikipedia page. The Wikipedia page and birthday is collected to be able to determine the **[zodiac sign](https://askastrology.com/zodiac-signs/)** of every person and also establish to which **[element](https://astrostyle.com/learn-astrology/the-elements-fire-earth-air-and-water-signs/)** the sign belongs. This information is stored in a dataset compressed in a 82.23MB pickle file. For more detailed information, please visit the **[Data Gathering notebook](https://github.com/simoneengelbr/twitter_zodiac/blob/main/DataGathering.ipynb)** and **[Explainer notebook](https://github.com/simoneengelbr/twitter_zodiac/blob/main/Zodiac.ipynb)** .

# **<span style="color:#8a7e4a">What does the network look like?</span>**

Before starting an in depth analysis, it's a good idea to first see what the network looks like. A total number of 2037 nodes and 124721 links constitute the network. Each node represents a Twitter user, colored by zodiac sign, and each link represents how users are connected by follows. In other words, this networks shows who is following who. Notice that some of the nodes are bigger than the others, this is because some people follow a lot of other people, like Barack Obama(598K), and some of them do not follow that many at all, like Cristiano Ronaldo(52). There are even cases when a personality does not follow anyone back, which is the case for Taylor Swift, Eminem, Adele, and more.
 
<p align="center">
  <img width="1200" height="950"  src="https://raw.githubusercontent.com/simoneengelbr/twitter_zodiac/main/docs/TransparentNetwork.png?token=AK2UC2M5B4KT5JPRRZZXPNS73IIAU">
</p>

The in-out degree distribution graph is another way of showing how people interact with each other. In-degree can be interpreted as the popularity of the personality among the other users of the platform and the out-degree the interest that a specific user has in another accounts. Usually we tend to follow the accounts that we find interesting. 

<p align="center">
  <img width="1200" height="450" src="https://raw.githubusercontent.com/simoneengelbr/twitter_zodiac/main/docs/TransparentInOutDegreeDistribution.png?token=AK2UC2LNLJB2HSDV3TER74273IKWO">
</p>

# **<span style="color:#8a7e4a">Content analysis</span>**

When it comes to the language used, in the social media area it is very personal. This is because when someone writes on the internet, that person is actually stating his opinion. Taking into consideration the astology factor, it is assumed that some zodiac signs tend to be more sensible, some more harsh, while others don't even want to share what they truly think with other people. To get a better understanding 

## **<span style="color:#8a7e4a">Water</span>**
![ElementWater](ElementWater.png)
  
## **<span style="color:#8a7e4a">Earth</span>**
![ElementEarth](ElementEarth.png)
  
## **<span style="color:#8a7e4a">Fire</span>**
![ElementFire](ElementFire.png)
  
## **<span style="color:#8a7e4a">Air</span>**
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
  <img width="1200" height="450" src="https://raw.githubusercontent.com/simoneengelbr/twitter_zodiac/main/docs/Transparent.png?token=AK2UC2IQNKKA34VJIBFNOI273IT7I">
</p>



