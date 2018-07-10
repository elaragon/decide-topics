# Decide Topics

[Decide Madrid](http://decide.madrid.es/) is the civic tech of Madrid City Council to create and support online petitions.
Despite the initial success, the platform is encountering problems with the growth of petition signing because petitions are far from the minimal number of supporting votes they must gather.
Previous analyses have suggested that this problem is produced by the interface: 
- Petitions are shown in a paginated list sorted by the _Hot score_, a non-optimal ranking algorithm. This method was devised to rank news items on Reddit whose interest usually declines rapidly, while online petitions require longer visibility to engage thousands of citizens and hence reach the threshold.
- Petitions are shown regardless of the user preferences and, therefore, many of them might not be of interest to every specific user.

To overcome these problems, this interactive system combines two modules to discover and explore two types of items:
- **Topics**: The alternative web interface starts with a query form to force users to explicitly set their interest. Then, matching petitions are retrieved and then grouped into topics with the text clustering method [Carrot2](http://search.carrot2.org/stable/search). Resulting topics are presented in a mosaic plot as polygons (sized by the sum of the number of votes).
- **Petitions**: Once a topic is selected, corresponding petitions are shown as circles (sized by the number of votes).

More info about this tool can be found at:
- [Aragón, P., Bermejo, Y., Gómez, V., & Kaltenbrunner, A. (2018). Interactive Discovery System for Direct Democracy. Advances in Social Networks Analysis and Mining (ASONAM). Barcelona, Spain.]()
- [Aragón, P. (2017). Datos para la participación. Un año en un día. Madrid, Spain.](https://www.youtube.com/watch?v=aXcF2zg3eVc&t=1s)

![alt text](https://raw.githubusercontent.com/elaragon/decide-topics/master/img/topics.png)
![alt text](https://raw.githubusercontent.com/elaragon/decide-topics/master/img/petitions.png)

## How to use it

The system is based on a Solr server and requires the corresponding packages (e.g. Java). 
Once the environment is ready, run the system locally:

```
bin/solr start -p 8080
```

Finally discover topics and petitions using a web browser:
```
http://localhost:8080/topics/

```

## Acknowledgments
This work is supported by [Medialab Prado](https://www.medialab-prado.es) and the Spanish Ministry of Economy and Competitiveness under the [María de Maeztu Units of Excellence Programme](https://www.upf.edu/icaria-cei/en/news/1027.html) (MDM-2015-0502). We would like to thank the team at [Participa LAB](https://www.medialab-prado.es/laboratorios/participalab) for their valuable feedback which served to improve this system.

