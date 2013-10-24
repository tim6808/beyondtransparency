--- 
layout: chapter
title: "Open Data in Chicago: Game On"
chapter: 2
part: 1
author: 
   -
     name: Brett Goldstein
     job: Former Chief Data Officer 
     employer: City of Chicago
     photo_url: /images/authors/brett.png
     twitter: bjgol
     about: "Former Chief Data and Information Officer for the City of Chicago. Currently a fellow in Urban Science at the University of Chicago Harris School of Public Policy."

permalink: "/part-1/open-data-in-chicago-game-on/"
featured: true
---
Before I joined Chicago’s government administration, I knew very little about open data. I certainly had been immersed in the world of data and analytics for some time, but I didn’t substantively understand the concept of “open” as it applied to this context. In fact, because I’d worked at the Chicago Police Department in the Counterterrorism and Intelligence Section, open data seemed completely counterintuitive. So when Mayor-elect Rahm Emanuel’s transition team reached out to me to discuss ramping up an open data program at the City of Chicago, I had to do some quick and hasty internet research to be properly prepared.
在我加入在芝加哥市政管理中心之前，我對於公開資料的認知並不多。

雖然當時我已經埋頭於資料分析的領域許久，但我並沒有實質了解公開資料中所對於”公開”的概念，事實上，當時因為當時我正要去芝加哥警局的反恐和情報組服務，公開資料在此似乎又不是有那麼直接的關係(開放的數據似乎完全反直覺的。

所以當新任市長伊曼紐爾的市政籌組團隊找我討論並且籌措芝加哥市的公開資料計畫，對此我不得不去網路上簡單花些功夫研究一下。
During the mayoral campaign, Mayor Emanuel had held an event at Microsoft that highlighted the importance of open government, citing open data at the heart of his vision for a more transparent Chicago. The mayor then asked me to serve as the city’s first Chief Data Officer (CDO) and to implement his vision of a more transparent government that not only makes its data available to the public, but also uses data analysis as a tool to inform policy and improve services.

The new administration started on May 16, 2011, with open data as a top priority from day one. The weekend prior, the policy group had gathered to discuss the strategy for the first hundred days and open data was listed as an early goal. My mission was to take the bones of the city’s existing program and make it a cornerstone of the city’s transparency initiatives. My first step was to assess what existed and then decide where I wanted to take the vision and direction as the CDO for the City of Chicago.

Before we dive into the details of what ensued, it is worth discussing the simple point that Chicago was the first major municipality to appoint a CDO. This was a clear and immediate statement about the importance of these initiatives to the new administration. Mayor Emanuel had decided early on that he wanted a team that used the city’s vast and rich data resources as a tool and that empiricism would inform policy. To achieve that goal, he created a senior-level post within his office that would focus on exactly that. By creating a CDO as his proxy for a data-driven and transparent government, Mayor Emanuel laid the foundation for Chicago to go from lagging behind other governments to being at the forefront of open civic data and transparency.

The City of Chicago did have an existing open data program so I wasn’t starting from scratch. Prior to the new administration it was managed by Danielle DuMerer, a project manager in The Department of Innovation and Technology (DoIT). The city had already secured the Socrata platform and kicked off some basic dataset projects—specifically, publishing logs of the Freedom of Information Act (FOIA) requests submitted by the public, as well as an assortment of facility and geographic datasets.

DuMerer had substantially engaged the local open government community with the city’s open data. However, the prior administration had not identified the open data program as a top priority among other competing issues, and even with DuMerer’s efforts the program struggled to gain significant traction. But once the new administration came on board with a clear mandate from Mayoral Emanuel to make open data a priority, the city’s open data program began to immediately change.

In the first two weeks as the city’s Chief Data Officer, I did my best to learn the ins and outs of the program I had inherited. I found it frustrating that the data platform had already been chosen. While I appreciate the turnkey efficiency of Socrata’s platform, I knew that a proprietary application would become a long-term financial investment. I am also a strong believer in utilizing open source technologies and was disappointed that we were doing little to support the community around CKAN, a widely used open source open data catalog. But because I needed to deliver results immediately, I was not in a position to make a sharp pivot. It wasn’t practical to consider other alternative platforms at that point.

There were also the upcoming Apps for Metro Chicago contests, plans for which had been initiated during the prior administration. The John D. and Catherine T. MacArthur Foundation was funding three thematic competitions to encourage businesses and software engineers to use City of Chicago and Cook County open data to create useful applications for residents. We greatly appreciated the philanthropic support of this initiative, but the competition imposed a hard timeline to roll out our program. 

It would have been simple to give it just enough attention to meet the requirements of the project and not offend the supporting foundation, allowing us to focus on the ideas coming from the new administration. However, we ended up seeing this competition as a great way to help launch the new open data program in Chicago and it helped us get momentum quickly. (MacArthur has continued to be a fantastic supporter of these forward-thinking programs.) Kicking off the Apps for Metro Chicago competition so soon after the start of the new administration was consistent with the strategy of rapidly expanding the existing open data program.

We immediately found that while technology was relevant to the project, clear executive sponsorship allowed for this initiative to rapidly accelerate. We achieved a couple of key milestones early on that ended up laying the foundation for the future of the program.

First, the city released its crime incidents dataset. Historically, crime data was hard to obtain in Chicago. While Chicago had been a leader in front-facing technologies, its raw data was not easily accessible. The Chicago Police Department’s CLEARpath website offered ninety days of historic incident-level crime data via a mapping interface and was a great start in terms of information access. However, if third parties wanted to use the data, they had to do a substantial amount of scraping.

Crime data is historically one of the most demanded datasets and is often too limiting in a few different ways: it is of too short an interval to provide utility for anything other than immediate-term situational awareness; the data is aggregated at a unit of analysis that is too dilutive (à la district, ward, or precinct); and/or the data is not machine-readable.

Chicago endeavored to solve all of these issues in one swift move. The designed release sought to open all incident-level crime data from January 1, 2001, to the present and update the dataset on a twenty four-hour cycle. Holding 4.6 million records, Chicago’s published dataset would be the largest automatically updating set of incident-level crime data ever released.

The technology behind the release was not complex, but nor was it trivial. Crime data is recorded in the Chicago Police Department’s transactional system and then replicated into their data warehouse. Our approach was to fire an ETL (a set of database functions for moving data from one place to another) from an internal utility server to pull data from the police warehouse and load it into the city’s data portal via Socrata’s API.

However, along the way, a couple of critical items needed to happen in order to ensure that the data was secure and could be rendered into a releasable form:

* The addresses needed to be block-reduced to protect privacy.
* Spatial coordinates also had to be scattered to assist with privacy protection.
* Updates needed to be captured and replicated into the dataset as the source system records were updated.
* Since the crimes dataset was to be one of their first large datasets, the Socrata platform needed to be able to efficiently handle uploads, updates, and queries.

We successfully completed all of these steps, experiencing some pain along the way, but the process eventually came together. As of April 2013, the dataset includes nearly 5.2 million records, continues to be automatically updated daily, and serves as a good example of the implementation of open data.

This data release brought substantial attention to Chicago’s open data program, much of which was due to the press around that release. Sophia Tareen, a reporter with the Associated Press, covered the story. She wrote a thoughtful piece on the enormity of the release and noted that it was a clear turning point for Chicago (Tareen, 2011). While written locally, the article was sent out en masse by the AP and, within a few hours, became an international story. As a result, Chicago’s open data program became very real and was validated by the broader community. We learned that there is enormous benefit to a high-profile release of a high-interest dataset early on. I view this as another seminal moment for the program, providing a solid foundation from which to launch. This release worked very well for Chicago, and I suspect it would work for other jurisdictions as well.

Second, the Apps for Metro Chicago competition provided a framework to engage the Chicago community. The competition demonstrated that many Chicagoans were deeply excited about open data and really wanted to engage with government to build tools to help their neighbors. In order to achieve the latter, we had to provide data in machine-readable formats, and it needed to be consistently refreshed. Prior to the re-launch of Chicago’s data portal, data had been made available, but usually in the form of a PDF, which technologists know can be somewhat less than friendly.

Our release of street sweeping data during the Apps for Metro Chicago contest window exemplifies this change. While at a Google-hosted open data hackathon in 2011, Scott Robbin approached DuMerer and I to ask about the city’s street sweeper dataset. He was interested in building an application that would notify users the night before their street would be swept. I thought this was a fabulous idea, since I had personally received a series of tickets for failing to move my car. However, the path from idea to implementation required some of the city’s data. The street sweeping schedule existed, but it was not published in a format easily used by software engineers or technologists. The Department of Streets and Sanitation had taken an Excel spreadsheet and created a calendar, using the software’s formatting tools. The resulting spreadsheet was then printed to a PDF and posted on the City of Chicago’s website. This format made it impossible to reverse engineer. Fortunately, in situations like these, interns are great at assisting with the tedious, but critical, work of converting an unusable file into one that can serve as a data source. We posted the resulting file on data.cityofchicago.org. From there, Scott produced an excellent site, sweeparound.us, which has assisted many of us in being mindful of the city’s cleaning schedule.

The sweeparound.us story exemplifies a couple key lessons that continue to hold true. First, we, as a city, needed to learn to produce data in machine-readable formats as part of our standard business practices. Second, a variety of communities demonstrated an enormous appetite for government data, including civic developers, researchers, and journalists. We saw the emergence of the civic developer community both in the philanthropic and for-profit models. Places like Chapin Hall at the University of Chicago had been struggling for years to extract administrative data for the purpose of research. Open data programs make it substantially easier, removing the need to negotiate non-disclosure or other types of agreements. Open data also has also stimulated new research. A Ph.D. candidate tweeted her gratitude at finally being able to finish her dissertation, and more traditional organizations have now embarked in multi-year studies, based on what has been released on the City of Chicago’s data portal.

The last lesson is one coined by Tim O’Reilly (2010): “Government as a Platform.” I did not completely understand this idea for some time, but now it’s one I greatly appreciate. Chicago’s data portal is designed to provide raw data in machine-readable formats. By providing an API to this data, any developer can access, use, or integrate all of this raw material for whatever purpose they can imagine. As the City’s Chief Information Officer and CDO, I purposely tried to avoid getting into the app development business and, instead, preferred to grow the portal to offer both diversity and depth. This strategy prevents us from being in the business of maintaining apps that require various programming skill sets and ongoing financial resources. Instead, a standards-based data portal allows us to be the platform, as O’Reilly suggests, and support the innovative ideas cultivated by various communities.

### Successfully Implementing an Open Data Program

After two years of building a successful program in the City of Chicago, there are a series of critical points that can be leveraged as other cities consider implementing or expanding open data.

#### Architecture

Building a large, useful, machine-readable, and meaningful data portal is a non-trivial technical task. First, of course, comes the question of platform. You will need to reflect on your staff’s capabilities, along with available funding to make this decision. Here are some points to consider.

If you need a turnkey solution, there are few options are available. Socrata is the dominant platform, and they are good at what they do. They provide a ready-to-go data portal. For organizations who cringe at the idea of building their own servers and using open source, this is the method that is going to work best for you. However, as we will discuss later, in order to have a sustainable open data platform, you are going to need to do some rather advanced work.

Beyond the platform comes the source of the data. For programs that are still in their most basic stage, using a turnkey approach can make this work incredibly easy. Your data may reside in something as simple as a spreadsheet. You can upload that information into Socrata directly and be ready to go in seconds, but it rarely remains that simple once you get beyond the basics.

Much of the data that you have will come from transactional or warehouse systems, and if your world is like mine, many of them are quite aged and somewhat cryptic. You will need to find ways to extract the data, understand what it means, and load it into the platform. This is somewhat less turnkey than you might originally think.

You also need to consider how much data you will be moving and how that will impact your enterprise network, storage, and systems. If you are simply dealing with something like a salary list, which is small data, the issue is trivial. However, what if you want to load something like GPS coordinates of your assets? In Chicago, that would be approximately ten million rows a day. That would stress most environments.

#### Sustainability

It may seem odd to call out this very specific point, but I suspect it is one of the most critical: the sustainability of the overall design. An open data program that relies on a human to keep it updated is fundamentally flawed. Considering that one of the goals of open data is transparency, it’s important to ponder the role of the middleman. I like to joke that people are often shocked when I tell them we do not vet the data before it gets released onto the portal. There is, in fact, no little dude in the basement of City Hall that checks every row of data before it goes out the door. That is the beautiful part of the design behind the portal.

Ninety nine percent of the data that goes onto data.cityofchicago.org arrives there automatically. Each one of the datasets has an ETL job that connects into the source system, takes the data, transforms it as appropriate, and loads it into the platform. This happens daily or more frequently. In some cases, we overwrite the entire set. For others, like crime incidents, we do an incremental update that adds new records and catches changes to existing records. This type of architecture accomplishes a series of critical points.

First, it is scalable. It is impossible to have millions of rows of data available based on manual refreshes. This makes little sense and will not be timely. Second, as mentioned before, it keeps the platform honest. Lastly, it creates sustainability. The program ceases to become about a single individual and, instead, becomes a programmatic area within the technological organization.

#### Fear

There is a strong institutional fear of open data. In a culture of “gotcha” journalism, the idea of something being disclosed that could embarrass an administration is a common worry and, therefore, barrier. It is often a reason to not release data. My experience with this highlights a couple critical points.

We have released millions of rows of data to date, and so far, it has gone very well. Every time the internal constituency has been concerned about a release, we have been able to push it forward and go public without incident.

It is critical that you develop a strong relationship with your open government community. By fostering this dynamic, you are able to create a “let’s make it work together” ethos. I explained that if every mistake I made got blown into a major incident, it would stymie our collaborative goals. In Chicago, they took this to heart. We created a team effort, working with Joe Germuska from the Northwestern University Knight Lab, and formerly of the *Chicago Tribune*, along with Daniel X. O’Neil of the Smart Chicago Collaborative. We would regularly convene via Twitter, email, phone, or at meet-ups. This worked out particularly well as we strived to conquer large and complicated datasets. These are the types of datasets that are very hard to release perfectly the first time.

Often, you will see a dynamic between government, the press, and the open government community that can be less than pleasant because of this “gotcha” concept I mentioned prior. Government releases something that has an error in it, and it becomes a “thing.” Maybe there is substantial press around the error or, even worse, it is viewed as being deceitful. Within this framework, there are typically only two strategies that can be taken by government. The first is to not release any data, which is not the optimal track for any of our interests. The second is to ensure that the data is one hundred percent perfect before it goes out the door.

The one hundred percent perfect model is fine when the data is small. If you are posting a spreadsheet with one hundred rows and it is not terribly wide, you can go through each and every line to ensure that it’s perfect. You can even scale the exercise to thousands of lines using a variety of mechanisms. However, what happens when the dataset includes millions of rows and covers a decade? Even with scripts and audit techniques, you cannot reach the one hundred percent confidence mark. This leaves most people in a quandary. When you want to release big and important data and you cannot ensure it is one hundred percent correct, it leads to all sorts of drama. It becomes a no-win situation.

This is where we changed the dynamic in Chicago so that we would be able to move the open data program into high gear. It came down to me personally developing a series of relationships within the community and investing the time to ensure that people understood and believed in what we were trying to do. Historically, a high-level member of the administration does not show up at an open government meet-up to discuss open data, but this was what ultimately enabled me to build trust between these entities. It also helped to have contacts like Joe, within the news organization, that allowed for the relationship building. These people believed that our open data plan was bigger than the single story and that we were building a broader system.

### Becoming Part of Day-to-Day Operations

As the open data program in Chicago became a robust and useful platform, the question came as to how we should take it to the next level. In the beginning of 2013, the mayor decided that he wanted to make a policy commitment to ensure the sustainability of the program. He issued an Open Data Executive Order (2012-2) that mandated that each department would designate an Open Data Coordinator, the city would create and sustain the position of Chief Data Officer, and there would be annual accountability as to the release of open data for transparency and sustainability (Emanuel, 2013).

The release and exposure of this executive order served to reinforce the hard work that had gone into the creation of the program. The ordering is one that would remain an open question for administrations that are looking to move forward in the realm of open data. Does it make sense to issue the executive order or legislation prior to the beginning of the initiative, or does it make sense to allow for some traction and then create that framework around it?

My preference is around the latter, but, clearly, I am biased. My thoughts focus on the ability to iterate and develop in an incubator environment before it becomes part of the system. Open data programs will have to evolve and grow in different ways in various cities. Lessons that apply to Chicago may not be relevant for a different city. The autonomy to try, explore, and adapt makes a lot of sense and is certainly a model that can be conducive to success. It is critical to create a viable program before becoming overly prescriptive about its functions.

### The Bare Minimum to be Successful

In order for an open data program to be truly successful, it requires two key items that are, in fact, also a broader lesson for many government initiatives. The first is the clear and vocal support of the executive sponsor—whether this is the president for the federal program or, in the case of Chicago, the mayor. With the unequivocal support of the mayor, roadblocks disappeared as it became clear that all parties would be accountable for the success—or lack thereof—of the program.

The second is financial support. A mandate with a lack of supporting funding in government is not, in fact, a mandate. There is a common saying in municipal government: “Control is based on a budget line.” Whoever controls the budget line controls the project. Chicago committed funding (not a large amount, but funding nonetheless) and resources to ensure that this could be successful. In the case of Chicago, this was able to fund the Socrata platform as a foundation and the ongoing work that was required for ETL development. Without a data platform and some sort of automated way to continue to keep it fresh, it is not a true program that will be sustainable beyond the individual.

I will, however, note the corner case that invalidates my second point, and this is, of course, a model that I admire: the scrappy do-it-yourself shop. In this scenario, the program is based on the open source CKAN model. The entity can build out their open data system on top of that platform. Seeing that they already have shown the innovation to work with open source software, it may be the case that they have the ability to write their own ETLs or leverage some of the great open source ETL tools that are available on the internet. From there, it would be a function of what sort of infrastructure could be built out. There is absolutely no reason a low-cost cloud solution couldn’t be implemented. This type of presence does not require a substantial amount of security, as you are not really worried about accessing the data. Rather, you simply want to preserve its integrity.

This corner case is somewhat interesting, as one can envision a scenario where one partners a strong executive sponsor with a scrappy technologist. Given access and mandate, it would be extraordinarily low-cost for a successful initial foray into the open data space. This is an area that we should be mindful of and find ways to support.

Chicago is an excellent case in showing how one can build an open data program where it is not expected. The role of the strong executive sponsor is critical to a program’s success, and Mayor Emanuel played that part. Building close partnerships with the community and strategic media attention were also key components of our success. Through tenacity and sustainable execution by the team, Chicago has been able to put forth an initiative that has become the gold standard in open data. These lessons from Chicago’s rapid scaling up of our program will help inform the next generation of open data initiatives, as new models for growth and sustainability of open data emerge.

### About the Author

Brett Goldstein is the former Chief Data and Information Officer for the City of Chicago. In 2013, he was named the inaugural recipient of the Fellowship in Urban Science at the University of Chicago Harris School of Public Policy. Before his appointment as Chicago’s first Chief Data Officer, he founded the Chicago Police Department Predictive Analytics Group. Previously, he spent seven years in the startup world building online real-time restaurant reservation service OpenTable. Goldstein is currently pursuing his PhD in Criminology, Law and Justice at the University of Illinois-Chicago.

References

O’Reilly, Tim. (2010). Government as a Platform. In Open Government. Retrieved from http://ofps.oreilly.com/titles/9780596804350/defining_government_2_0_lessons_learned_.html
Emanuel, Rahm, City of Chicago. (2013). Open Data Executive Order (No. 2012-2). Retrieved from http://www.cityofchicago.org/city/en/narr/foia/open_data_executiveorder.html
[Tareen, S. (2011, September 14). Chicago to publish crime stats online. The Washington Times. Retrieved from http://www.washingtontimes.com/news/2011/sep/14/apnewsbreak-chicago-to-publish-crime-stats-online/?page=all](http://www.washingtontimes.com/news/2011/sep/14/apnewsbreak-chicago-to-publish-crime-stats-online/?page=all)
