  * Traffic Control Terminology
    (TODO: dew Build/find a diagram to talk to about the sentences below, place them into the presenter notes and figure out how to summarize)

    + Delivery Service (DS)

      - One to one mapping to the FQDN that is used as a hostname to delivery content.  

      - Many options and settings regarding how to optimize the content delivery are configurable on a DS basis.
 
    + Cache Group (CG)

      - Logical group of caches that Traffer Router uses as a combined cache

    + Localization
      
      - Traffic Router finds the right Cache Group for a client using a coverage zone file (.czf) to route the client to the closest Edge Cache.

    + Content Affinity

      - Traffic Router finds the right server in a Cache Group for the requested content based upon the URL Path for HTTP DSes and on the hostname for DNS 
        DSes to select the same cache for the content if possible using consistent hashing.

      - ATS uses consistent hasing in parent selection and origin selection (in Multi Site origin) to select the same parent for the same content if possible.
 
    + DNS Content Routing

      - For a DNS Delivery Service the client receives a URL with a hostname beginning with `edge.` (e.g. http://edge.hostname.cdn.com/foo/bar/fun.html).`

      - The LDNS server is resolving this hostname to an IP address, it ends at Traffic Router because it is the authoritative DNS server for cdn.com and the domains below it,
        and subsequently responds with a list of IP addresses from the eligble caches based on the location of the LDNS server.

    + HTTP Content Routing

      - For an HTTP Delivery Service the client receives a URL wiht a hostname beginning with `tr.` (e.g. http://tr.dsname.cdn.com/foo/bar/fun.html)`, the LDNS server resolves this hostname
        to an IP Address, but in this case Traffic Router returns its own IP address.

      - The client will now connect to Traffic Router's port 80 to get the content and Traffic Router will use a 302 to redirect to the best cache.

    + Health Protocol
     
      - Redundant Traffic Monitor servers operate independently from each other but take the state of other Traffic Monitors into account when asked for health state information.

      - The Health Protocol creates an optimistic view for Traffic Router for the DS and Cache statuses that are not consistent across all Traffic Monitor instances (peers).

    + Profile

      - a Profile is a set of configuration settings and parameters, applied to a server.  For a typical cache there are hundreds of configuration settings to apply.  The Traffic Ops parameter
        view contains the defined settings, and bundled into groups using Profiles.  Traffic Ops allows for duplication, comparison, import and export of Profiles.

    + Type

      - Type is an overloaded term in Traffic Control.  

        There are types defined for:
          - Server
          - Delivery Service
          - DS Regex
          - Cache Group
          - User
          - Extension
          - Federation
          - DSN Record type