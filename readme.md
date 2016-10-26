# Open Data Portal Technical Implementation Plan
## City of Asheville, NC
## October, 2016

### Background
On October 13, 2015 the Asheville City Council adopted a resolution “directing the City Manager to establish an open data policy for the City of Asheville for sustaining public data availability using open data standards.” The policy directed that the City’s Information Technology Services publish technical standards for publishing public data sets in raw or unprocessed form and a technical implementation plan. This document fulfills that directive.

### Technical Standards
There is near-universal consensus that the current standard for the delivery of raw, machine-readable datasets is a [REST](https://en.wikipedia.org/wiki/Representational_state_transfer) (REpresentational State Transfer) application programming interface (API) that returns data in either a comma-separated-value (CSV) or a Javascript Object Notation (JSON) format. The REST API is commonly supplemented by the ability to simply download the dataset as a file in either of the above formats. The [City of Asheville open data portal](http://data.ashevillenc.gov/) supports both delivery methods and both formats.

The new [GraphQL standard](http://graphql.org/) released by Facebook last year is seeing rapid adoption as a powerful alternative to REST that better reflects the relationships between different datasets, provides access to the underlying schema,  and offers greater control to data clients over what information should be delivered. In Phase 2 of the implementation plan below, the City of Asheville will add a GraphQL API endpoint to the same data provided via the REST API.

### Implementation Plan
#### Phase 1 (Current): ArcGIS Rest Services
The unexpected failure of the existing open data portal in February 2016 necessitated an immediate decision on the open data infrastructure. In May, the City launched a new open data portal using ArcGIS Server. This new infrastructure represents a significant enhancement over the previous portal since ArcGIS server not only provides the REST API and file download serving both JSON and CSV, it also supports map and GIS functionality, convenient SQL-like query capabilities, and a built-in data viewer.
