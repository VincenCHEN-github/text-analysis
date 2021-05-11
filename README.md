# text-analysis

**Factors Affecting COVID-19 Vaccination and Social Media Discussion Research**


Department of communication, Hong Kong Baptist university

AIDM7350 AI for Digital Media Workshop

Dr. WANG Xiaohui

April 29, 2021

**Abstract**

Due to the impact of the COVID-19 epidemic, the research and development and promotion of the COVID-19 vaccine have received extensive attention. At present, only vaccines can protect us from this pandemic, and if we want to form herd immunity, we need to increase the vaccination rate and vaccine coverage. However, due to various factors, there are obvious differences in the global vaccination process.Therefore, we want to establish a regression model to study the impact of economic, political and social exchanges on the current status of vaccination in various countries. At the same time, we take the United States and India as representatives to analyze the differences in public attitudes and discussions on vaccines. Through R and LDA topic mining, we can obtain discussion topics from Twitter users in the United States and India, and observe the discussion focus and emotional trends of tweets. We collected a data set of the World Happiness Index shared by the United Nations and the World Health Organization that includes the country&#39;s per capita GDP, social support, healthy life expectancy and social freedom. And also collected data on the number of vaccinations in each country as of April 19 and discussions on vaccines on social media.

_Key words:_ COVID-19 vaccination, social media, sentiment analysis

**Background**

Under the influence of the COVID-19 epidemic, the vaccination work has received widespread attention worldwide. Large-scale vaccination of the COVID-19 vaccine is spreading all over the world. So far, at least 135 countries have participated in the vaccination work, and the total injection volume of various vaccines has reached 450 million doses. This will be the largest and fastest mass vaccination operation in human history. Some countries have seen the effect of popularization of vaccination, and the number of new infections and severe hospitalizations has been significantly reduced. At the same time, the establishment of the immune barrier means that the protective efficacy of the vaccine has a great relationship with the population&#39;s vaccination rate. When the vaccination reaches 70% and above, the group protection effect can be produced, and the vaccination rate is only about 10%, which can only protect the individual and cannot produce the group immunity. An epidemic will occur when a source of infection is introduced, which is why it is necessary to promote vaccination and increase vaccination coverage.

However, the progress of COVID-19 vaccine vaccination in different parts of the world has significant differences. At the beginning of December last year, the United Kingdom became the first country in the world to approve the large-scale use of BioNTech&#39;s COVID-19 vaccine. It has been four months since now. Tens of millions of people have already been vaccinated, but this is in rich countries, in low-income countries, the number of vaccinations is even less than hundreds. Almost all countries in Europe and the United States have begun mass vaccination, but only a few countries in Africa have begun to promote it. Many places are still waiting for the first batch of vaccines to arrive in their country. Another example is Israel&#39;s COVID-19 vaccination rate has remained the highest in the world, while China&#39;s vaccination rate is only 4%. The daily vaccination rate for 100 people worldwide has reached 0.1 doses. Among them, the vaccination rate per 100 people in Chile and Israel has exceeded one. Although the number of COVID-19 vaccines in our country is large, the coverage rate still needs to be improved. There are many factors that affect the vaccination rate, and it is also a complicated process. Which involves political economy, human factors, scientific research and development, production, storage and transportation and many other factors.

The above reasons have aroused our attention, and there may be many influences behind the vaccination rate. Our group will start from several aspects such as GDP per capita, social support, healthy life expectancy, free choice of life, and in-depth study of the reasons behind the impact of the vaccination rate.

**Method**

The vaccination situation of vaccines is affected by various factors. From the national level, due to economic and political reasons, the vaccine production capacity and vaccine purchasing capacity of each country are different. From the level of society and individual citizens, their attitudes towards vaccines, The recognition of the effect and the level of social public health services will affect the vaccination situation. On the other hand, the current development of social media and the Internet affects people&#39;s attitudes and choices about major public events, and public opinion also affects the public&#39;s selection of vaccination(Oku, A., Oyo-Ita, A., Glenton, C., Fretheim, A., Eteng, G., Ames, H., ... &amp; Lewin, S, 2017) . This study hopes to establish a regression model to study the impact of various economic, political, social and communication factors on the current vaccination situation in various countries in the world. At the same time, the United States and India are used as representative cases of higher and lower vaccination rates to analyze the differences in attitudes and discussions.

**Data Collection and Processing**

The data in this study comes from shared data sets such as the United Nations, WHO, etc., and collected data on the World Happiness Index, including per capita GDP, social support, healthy life expectancy, and social freedom levels in each country, as well as the number of vaccinations and the number of vaccinations used in each country as of April 19. Vaccines and other data, and we collect discussions on vaccines in social media. We have collected recent tweets about the COVID-19 vaccines used in the entire world on large scale. According to the vaccine names of various brands that have been approved for marketing, the content of tweets crawled through search operations, including user ID, user location, and publication Time, tweet text and other content, as of April 19, 2021, a total of 65,089 entries. In order to study the impact of various factors on vaccination, we selected the top 20 countries for the total amount of vaccination for analysis based on the data released by the BBC real-time monitoring platform. Therefore, we manually clean and filter all tweet data, and divide the tweets from 20 countries and regions based on the country. The amount of data is as follows:

| Country | Sample Size | Country | Sample Size | Country | Sample Size |
| --- | --- | --- | --- | --- | --- |
| United State | 3623 | France | 265 | Canada | 1766 |
| China | 962 | Russia | 481 | United Arab Emirates | 265 |
| India | 6263 | Italy | 105 | Poland | 12 |
| United Kingdom | 3119 | Mexico | 30 | Saudi Arabia | 27 |
| Brazil | 15 | Chile | 44 | Bangladesh | 97 |
| Germany | 284 | Spain | 74 | Argentina | 28 |
| Turkey | 41 | Israel | 80 |
 |
 |

In order to quantify the public&#39;s sentiment about vaccine discussions in social media to analyze whether it has an impact on the country&#39;s vaccination situation, we use Python to program and Textblob to quantify the sentiment of each tweet text, and get a value of -1 to 1.The sentiment value of all tweets in each country is averaged to get the sentiment value of public discussion in that country.

**Data Analysis**

_ **Regression analysis** _

O ![](RackMultipart20210511-4-12nmp7u_html_79df25205d41748c.png) ur data analysis includes two parts. The first is to take the per capita GDP, social support level, healthy life expectancy, social freedom level, and sentiment value as independent variables. Because the time of the start of vaccination varies in different countries, the duration of vaccination is different, so the time factor Independent variables are also added, and the number of doses per 100 people is used as the dependent variable to establish a regression model to observe the influence of various factors on the vaccination situation. It can be seen from the way that the regression effect of the sample is better.

_ **Text analysis** _

On the other hand, in order to analyze the differences in public attitudes and discussions about vaccines, we will select typical cases for comparative research. Since both citizens of the United States and India have Twitter users, and the current number of vaccinations in the United States is relatively large, and the number of vaccinations in India is relatively low, this study takes the United States and India as representative cases of higher and lower vaccination rates for their countries. First of all, this project uses RStudio as a tool and uses LDA topic mining technology to observe the topics of the discussion content from the United States and India, and find the optimal number of topics to be 7, thereby mining 7 topics to observe the focus of the discussion. And then we analyze the social media tweets, and conduct research on the amount of discussion, discussion content, emotional trends, etc., and find the differences.

**Results**

**Regression Analysis**

|
 |
 | Vaccination rate |
| --- | --- | --- |
| Pearson | Vaccination rate | 1.000 |
| --- | --- | --- |
|
 | Logged GDP per capita | .448 |
|
 | Social support | .371 |
|
 | Healthy life expectancy | .217 |
|
 | Freedom to make life choices | .090 |
|
 | Vaccine release days | .624 |
|
 | emotion | -.048 |

From the above table, we can find that the overall value is small. This may be because our sample size is only 20 countries and does not have power, but we can still draw some conclusions.

Vaccine release days have the highest correlation with the vaccination rate, which is 0.624. This means that the earlier the vaccine program starts, the more days there will be for promotion, and therefore the greater the number of people vaccinated.

Logged DAP per capita is followed by 0.448, which is likely because countries with a higher GDP per capita are more economically and technically powerful, have the know-how to develop vaccines or have the money to import vaccines from other countries.

Social support usually refers to the mental or material help and support given to individuals from all aspects of society, including family and friends, and its correlation with the vaccination rate is 0.371. This may be because the public welfare policies of some countries provide help for vaccination，or some countries have received vaccine funding from other countries.

Healthy life expectancy has a certain but not high correlation with the vaccination rate, which is 0.217. It is possible that a country with higher life expectancy has more advanced medical technology and people attach more importance to health, which affects the vaccination rate to a certain extent.

The least relevant is Freedom to make life choices, which is 0.090. In the face of the virus, everyone is equal, and we do not have the freedom to choose not to be infected.

F ![](RackMultipart20210511-4-12nmp7u_html_6734a6e93be99689.png) ![](RackMultipart20210511-4-12nmp7u_html_18c50fe3d53d3dba.png) ![](RackMultipart20210511-4-12nmp7u_html_d5ca485f0710e2c9.png) ![](RackMultipart20210511-4-12nmp7u_html_29ba8f71f393d23a.png) ![](RackMultipart20210511-4-12nmp7u_html_8e647b2ffc6be818.png) ![](RackMultipart20210511-4-12nmp7u_html_912435b9c7836e1.png) inally, in this analysis, people&#39;s sentiment about vaccines on Twitter is not directly related to the vaccination rate, because opinions expressed on social media platforms do not necessarily reflect people&#39;s behavior in real life.

**Text Analysis**

_ **Discussion volume** _

![](RackMultipart20210511-4-12nmp7u_html_2feb0f4c950c941e.png) ![](RackMultipart20210511-4-12nmp7u_html_4ca973d373e152e1.png)

Discussion from United State Discussion from India

The above two graphs respectively record the trend graphs of the number of daily discussions about the COVID-19 vaccine by Twitter users in India and the United States from December 12, 2020 to April 19, 2021. It can be clearly seen that Twitter users in the United States have been more active in discussions about vaccines than those in India. The discussion of vaccines by Twitter users in India has changed with the changes in the number of people infected with the local epidemic. India has rapidly dropped from nearly 100,000 cases on September 28, 2020 to 8,697 cases on February 28, 2021. The number of daily infections once dropped sharply, just when the world believed that India had successfully contained the epidemic. In April, the epidemic in India began to rebound rapidly, and the number of discussions among users on Twitter also increased.

Twitter users in the United States discussed the increase in the number of vaccines, mainly due to the continued deterioration of the epidemic and the time of vaccination. In January 2021, the number of deaths from COVID-19 pneumonia in the United States set a new record. At the same time, it is reported that the distribution of vaccines in the United States is also in chaos, with more than 20 million doses of vaccines already distributed and missing. These have caused people to discuss on social media. Secondly, the United States began to gradually vaccinate specific populations on December 14, but to complete the entire vaccination, two injections are required, and the two injections are 21 days apart. By the end of January, the first batch of talents who completed all injections gradually began to discuss on social media.

_**T ![](RackMultipart20210511-4-12nmp7u_html_2c4a49356bf53ca4.png) opic of discussion**_

![](RackMultipart20210511-4-12nmp7u_html_89cad576f47701c9.png)

Topics from United StateTopics from India



We have conducted topic mining on vaccine-related posts posted by Twitter users in India and the United States. It can be clearly seen that there are certain differences in the discussion of the topic of vaccines between the two regions. The discussion on Twitter in India involves the political level between countries. Here you can see the emergence of China and Russia. Covaxin, a vaccine brand developed locally in India, has also appeared, and imported vaccine brands such as Pfizer and Johnson &amp; Johnson in the United States have also appeared. There is also a discussion about the government&#39;s vaccine policy and the dosage of people vaccinated. The overall discussion of Indian Twitter users tends to focus on the part of people&#39;s livelihood concerns.

The topic mining of Twitter users in the United States is more discussions about several common vaccine brands on the market. For example, Pfizer, Johnson &amp; Johnson, and AstraZeneca appear here. It can be seen that users are more concerned about the effects of these branded vaccines, the dose of vaccination and the length of interval between vaccination. The second is the follow-up specific situation after vaccination and how people feel about vaccination. Twitter users in the United States pay more attention to the discussion of the vaccine itself and how people feel after vaccination. It can more intuitively reflect the overall situation of the vaccine.

_**C ![](RackMultipart20210511-4-12nmp7u_html_27440469c0a62a71.png) ![](RackMultipart20210511-4-12nmp7u_html_e16ea078ead8557a.png) ontent of discussion**_

Content from United StateContent from India

We have also obtained two other word cloud maps that allow us to summarize the public attention of these two countries (USA and India) in general. In the specific context of vaccination, both Americans and Indians focus their attention resources almost exclusively on the two topics of vaccines or coronavirus. The difference is that Americans seem to focus more on the brand of the vaccine during this period. What we can reasonably infer is that Americans have more choice in vaccines because their vaccines are domestically produced. Although there were a number of unexpected conditions that occurred during the injection process, and of course these unexpected conditions certainly became the focus of public discussion. But what is undeniable is that the United States still has a global leadership position in biochemical pharmaceuticals.

In contrast, in India, their public attention is actually focused more on the vaccines available abroad than on the epidemic and the vaccines. We can see this from the words &quot;SputnikV&quot; and &quot;Pfizer&quot;, &quot;Moderna&quot; and other vaccine brand names. Of course, we can see that they clearly prefer to get the Russian &quot;SputnikV&quot; vaccine. This reflects India&#39;s deficiency in the field of biochemical medicine, although they have provided OEM services to some vaccine development countries since the launch of the vaccine. It is also worth noting that the Indian public is very concerned about their Prime Minister, Narendra Modi. We can see this in the size of the keyword &quot;Narendra Modi&quot;. This shows that Indians care a lot about the leader or his government&#39;s response to the outbreak or the vaccination efforts. The fact that so much public attention is focused on the Prime Minister of India reflects that the public wants to express their wishes or demands to the government regarding the vaccine or the epidemic. If the government were to pay attention to this desire or demand, then the government would change their media agenda setting and thus achieve a public agenda setting. In this way, the Indian government can shape the larger issue of vaccination among the public and ultimately achieve a synergy with the public. However, the reality is that the Modi government seems to have a hard time focusing on vaccination while opening up religious and folkloric activities that have led to the outbreak getting further out of control in India.

_**S ![](RackMultipart20210511-4-12nmp7u_html_b9acdd6e4587849d.png) ![](RackMultipart20210511-4-12nmp7u_html_101875d32c33bef.png) entiment**_ _ **a** __ **nalysis** _

Sentiment from United State Sentiment from India

In our sample, the amount of discussion on vaccines by Indian users on Twitter is higher than that in the United States, which to some extent shows that Indians are more concerned about the topic of Covid-19 vaccines may due to the current virus outbreak in India.

Twitter users in India and the United States have the same sentiment on the vaccine. The vast majority of tweets are neutral, followed by positive, and finally negative. Tweets with negative attitudes in the two countries are nearly half of those with positive attitudes. Although the overall number of tweets with negative sentiment is the least, the opinions of this part of the group cannot be ignored. In short, most people maintain a neutral attitude, but there is no guarantee that they will change their position in the future.

S ![](RackMultipart20210511-4-12nmp7u_html_9727c57e21893aa8.png) ![](RackMultipart20210511-4-12nmp7u_html_f3dd2c4f42f96b28.png) ![](RackMultipart20210511-4-12nmp7u_html_69eaef15f252d3c6.png) ![](RackMultipart20210511-4-12nmp7u_html_f5bee1b4d77a3d88.png) entiment from United State Sentiment from India

On Twitter in Indian, most of the discussion was about vaccine manufacturers, such as the Russian brand of vaccine &quot;SputnikV&quot; that was approved for use in India recently, which may have sparked the discussion. The &quot;Covaxin&quot;, a locally produced vaccine, and &quot;Covishield&quot;, an imported vaccine, were both appeared in Positive and Negative respectively. Therefore, it is difficult for us to distinguish the true evaluation of the two vaccines by users. But from the words &quot;safe&quot;, &quot;effect&quot;, and &quot;risk&quot;, we can infer that people discuss the safety and effectiveness of vaccines; from the words &quot;get&quot;, &quot;approv&quot;, and &quot;use&quot;, we can infer that people discuss how to obtain vaccines.

On Twitter in the United States, the most discussed topic is the &quot;moderna&quot; vaccine, which may be related to its positive and negative news. Moderna, for example, is the first Covid-19 vaccine to be published; Moderna was previously suspended by the World Health Organization because of severe allergic reactions. Similarly, a large number of the same words appear in Positive and Negative respectively, and it is still difficult for us to distinguish people&#39;s true evaluations. However, from the words &quot;effect&quot;, &quot;good&quot;, &quot;pain&quot;, and &quot;poison&quot;, it can be inferred that people have discussed the safety and effectiveness of vaccines. From the words &quot;side&quot;, &quot;arm&quot;, and &quot;feel&quot;, it can be inferred that people have discussed the side effects of the vaccine, such as pain in the arm after vaccination. It can be inferred from &quot;get&quot; that people are discussing how to obtain vaccines.

All in all, people on Twitter are more concerned about the effectiveness and safety of vaccines, as well as the way vaccines are obtained, which is related to the self-interest of most people. In addition, we can also find that different brands of vaccines are likely to be discussed and compared on social platforms.

_**S ![](RackMultipart20210511-4-12nmp7u_html_63adb4174c91aa24.png) ![](RackMultipart20210511-4-12nmp7u_html_c1c36525ade7c918.png) entiment trend analysis**_

Sentiment trend of United State Sentiment trend of India

The picture above shows the tweets about the COVID-19 vaccine from the United States and India from December 2020 to April 2021. It can be seen that the American public has greater emotional fluctuations in the discussion of vaccines. And overall, the emotional intensity of the discussion gradually increased. Neutral emotions are always the strongest, followed by positive emotions. At the same time, the gap between positive emotions and negative emotions is large and has a tendency to gradually increase. Only at certain times, such as mid-March and April 16 after the public is vaccinated. After the news of complications or death is released, the intensity of negative emotions is greater than or close to the discussion of positive emotions. The rest of the time period, the discussions are mainly positive. After April 16, it can be seen that the gap between positive and negative emotions continues. Increase.

The tweets from India showed a more stable emotional expression, and various emotions were always flat. At this time, India did not officially launch a large-scale vaccination work. As India announced on March 1 that more than 200 million ordinary people have begun to vaccinate Vaccines, the integrity of public discussions on social media, have exploded, and the emotions discussed at this time are more positive. However, the emotional intensity of the subsequent discussions decreased rapidly and stabilized. The discussion was generally positive, but the gap with negative emotions was small. Until the news release on March 16 that Australian vaccination patients died of thrombosis, negative emotions Discussions dominate the mainstream. The vaccination work in India has not been carried out smoothly and the vaccination rate is low. As the public is still far away from the vaccine, it is reflected in the fact that the public&#39;s emotional attitude towards the vaccine has not changed significantly, and the continuous out-of-control of the epidemic has also caused the public to discuss the vaccine. More negative.

**Discussion**

**Country**  **P**** erspective**

We looked at the following indicators to analyze the countries with the greatest correlation with vaccination rates among the 20 countries we screened. They are: social support, textual sentiment scores, recorded GDP per capita, healthy life expectancy, and freedom to make life choices. From the above results, we can see that the number of days of vaccine release has the highest correlation with the vaccination rate. Some countries that started vaccination earlier have higher vaccination rates. We can analyze four countries, such as the United Kingdom, the United States, Chile, and Israel. They either produce their own vaccines (such as the United States) or have established good political relations with major vaccine-producing countries (such as the United States or China).

For example, Israel&#39;s rapid access to vaccines may be due to the greater influence of Jews in the United States. The recorded GDP per capita is also an indicator related to a good vaccination rate. For example, developed countries such as the United States and the United Kingdom have higher per capita GDP, which leads to better social welfare. High welfare and strong social institutions can improve the efficiency of vaccination. Another group of countries such as the United Arab Emirates and Israel have high GDP per capita due to their small populations. A small population can also increase vaccination rates to some extent, because fewer vaccines are needed. In addition, social support will also affect the vaccination rate to a certain extent. For example, countries with an index of 0.9 or higher, such as the United Kingdom, the United States, and Israel, have a good welfare system, so they can provide more comprehensive care and support to disadvantaged groups. I think their vaccination will also give priority to disadvantaged groups. However, Western European countries such as Spain, Germany and France also have a social support index of 0.9 or higher, but the vaccination rate is not high. We think it might be because most of their vaccines still need to be imported, which slows down the vaccination process. Perhaps it is because of the refugee problem, because these countries are hosting a large number of refugees. Due to factors such as religion or low level of education, certain refugees from the Middle East who have been granted status may be anti-scientific. As a result, they are reluctant to be vaccinated, thereby reducing the overall vaccination rate. Finally, healthy life expectancy and free choice of life are the two least relevant indicators of vaccination rates. This is because healthy life expectancy is not only affected by medical care. Freedom to choose one&#39;s life is also difficult to explain, because the United States and China have high value, but the vaccination rate is very different. In both countries, the public has the freedom to choose whether to vaccinate, but it is clear that this indicator is too much affected by personal preference.

**Public**  **P**** erspective**

On the other hand, our research analyzes the differences in the discussion of the COVID-19 vaccine on social media among the public in two countries with very different vaccination rates. It can be seen that there are differences in the discussion of vaccines among the public in countries with different vaccination conditions, and this is reflected in different aspects of the discussion. First of all, countries with low levels of vaccination are less enthusiastic about vaccine discussions, and discussion of topics will only be triggered after relevant special events occur. The second is the content of the discussion. In countries with more vaccinations, the United States, its topics are mostly about the effects of vaccines and vaccination services, while India is mostly discussing related political and economic issues. Finally, on the emotional aspect of the discussion about vaccines, the American public&#39;s discussions are generally more positive and positive, with greater emotional intensity, while the Indian public&#39;s discussions have lower emotional intensity and higher negative sentiments.

**Research**  **Reflection**  **and**  **P**** rospects**

In summary, we believe that it is innovative to analyze different countries from the perspectives of social economy, public attention and public sentiment, and to explore and compare multiple countries from multiple dimensions. The references we used before can help us improve this research in the future. The difficulty of collecting accurate information about religion and race in each country prevents us from considering these two factors in our research. It must also be pointed out that because we are unable to collect information on the vaccination status of front-line medical staff in each country/region, we cannot analyze in the content below whether the medical community supports vaccination or whether it is affected by social media statements. Our report. We believe that if we are to conduct continuous and effective research, we should focus our research more on conspiracy theories that may be vaccinated on social media, and whether personal emotions are affected by false news. It is also important to track public attitudes towards vaccines to help public health agencies better understand the situation.

Reference

DeRoo, S. S., Pudalov, N. J., &amp; Fu, L. Y. (2020). Planning for a COVID-19 vaccination program. Jama, 323(24), 2458-2459.

Trujillo, K. L., &amp; Motta, M. (2020). A majority of vaccine skeptics plan to refuse a COVID-19 vaccine, a study suggests, and that could be a big problem. The Conversation.

Abbas, K. M., Kang, G. J., Chen, D., Werre, S. R., &amp; Marathe, A. (2018). Demographics, perceptions, and socioeconomic factors affecting influenza vaccination among adults in the United States. PeerJ, 6, e5171.

Logullo, P., Carvalho, H. B. D., Saconi, R., &amp; Massad, E. (2008). Factors affecting compliance with the measles vaccination schedule in a Brazilian city. Sao Paulo Medical Journal, 126(3), 166-171.

Oku, A., Oyo-Ita, A., Glenton, C., Fretheim, A., Eteng, G., Ames, H., ... &amp; Lewin, S. (2017). Factors affecting the implementation of childhood vaccination communication strategies in Nigeria: a qualitative study. BMC public health, 17(1), 1-12.
