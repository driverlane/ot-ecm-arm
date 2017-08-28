ot-ecm-arm

Azure Resource Manager templates for deploying OpenText ECM environments.

## components

Each ARM template has a markdown file explaining what the component does and the parameters it needs to run. Please refer to these for more information.

The current components and their relationships:
* OpenText Enterprise Content Management
  * Content Server
    * Remote Cache
      * Remote Cache server
    * Content Server front end server
    * Content Server admin server
      * Remote Cache smart services
    * SQL database
  * OTDS
    * OTDS server
    * SQL database
  * Archive Center
    * ???
    * SQL database
  * AppWorks Gateway
    * AppWorks server
      * Tempo
        * SQL database
      * ECM Everywhere
      * SQL database

Shared components:
* SQL server - needs to be either SQL farm or Azure SQL - intially only support Azure SQL
* Storage stuff
* Virtual network
* Firewall - though this may be implicit in each of the server templates
* CDN - load management/balancer

## thinking

Can this also maybe a better way for creating copies of environments? Rather than keeping the existing environment, they just blow it away and these templates support copying data from an existing instance. Yes is the answer, but how much work.