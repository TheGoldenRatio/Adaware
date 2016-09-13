We want to use a graph database to be able to represent a variety of things (words within a document and their relation to each other, keywords and their relation to documents, documents and their relation to each other, etc.). The easy answer is to go ahead and use a RDBMS like postgresql. In reality, this would probably be fine up to a point; simply have a table of documents/words (vertices) and table(s) of relations (edges).  

However, there's a lot of obvious overhead with this approach, such as the large join queries you'd have to do in order to traverse the graph. There's a fair amount of work to keep your schemas small in order to make these joins reasonable, but this is really just skirting the issue and trying to apply techniques to increase performance. Graph databases are the theoretical answer to this plethora of issues since they make navigating the graph easier and more efficient.  

There seem to be 3 major front-runners in the world of graph databases: Titan, Neo4j, and OrientDB.

## Comparisons
http://db-engines.com/en/system/Neo4j%3BOrientDB%3BTitan  
http://www.slideshare.net/kwoxer/orientdb-vs-neo4j-comparison-of-queryspeedfunctionality  
http://www.datascienceassn.org/sites/default/files/Empirical%20Comparison%20of%20Graph%20Databases.pdf  

## Titan
Titan seems to have [died off](http://stackoverflow.com/questions/28581602/which-graph-database-orient-or-titan-is-good-to-use-with-spring-and-liferay) many [months ago](https://github.com/thinkaurelius/titan/). The Aurelius team (builders of Titan) were acquired by Datastax, and as promised they've contributed little-to-no time to the project.

## OrientDB
https://news.ycombinator.com/item?id=9253488  
http://orientdbleaks.blogspot.com/2015/06/the-orientdb-issues-that-made-us-give-up.html  
There seems to be more than enough drama related to OrientDB to make any wary before they choose to use their software. The very same [Gartner post](https://www.gartner.com/doc/reprints?id=1-2PMFPEN&ct=151013) they're choosing to promote themselves also points to their issues (of course, they choose to highlight the positives, but bugs and support are the major issues). I think they have a lot of interesting technology, but the bottom line is that they've got so many issues it's hard to distinguish fact from fiction. In any case, so many stories don't just usually manifest themselves, so there's likely some form of fact between them.

## Neo4j
Who says all press is good press?! I guess by process of elimination it means Neo4j is the winner. However, not to be a debbie downer, Neo4j offers a host of exciting features. It's the most popular of all the options (perhaps for the above reasons) and the most mature of the options as it's been around for the longest. The real drawback is that it doesn't offer built-in clustering in the free version.

## Resources
http://tinkerpop.apache.org/  
https://www.digitalocean.com/community/tutorials/how-to-install-neo4j-on-an-ubuntu-vps  