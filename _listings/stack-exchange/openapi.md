---
swagger: "2.0"
x-collection-name: Stack Exchange
x-complete: 1
info:
  title: Stack Exchange
  description: stack-exchange-is-a-network-of-130-qa-communities-including-stack-overflow-
  version: "2.0"
host: api.stackexchange.com
basePath: /2.2
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /me/privileges:
    get:
      summary: My Priveleges
      description: "Returns the privileges the user identified by access_token has.\n
        \nThis method returns a list of privileges."
      operationId: returns-the-privileges-the-user-identified-by-access-token-has-this-method-returns-a-list-of-privile
      x-api-path-slug: meprivileges-get
      parameters:
      - in: query
        name: callback
        description: All API responses are JSON, we do support JSONP with the callback
          query parameter
      - in: query
        name: filter
        description: '#DiscussionThe Stack Exchange API allows applications to exclude
          almost every field returned'
      - in: query
        name: page
      - in: query
        name: pagesize
      - in: query
        name: site
        description: Each of these methods operates on a single site at a time, identified
          by the site parameter
      responses:
        200:
          description: OK
      tags:
      - Privileges
  /privileges:
    get:
      summary: Get Privileges
      description: "Returns the earnable privileges on a site.\n \nPrivileges define
        abilities a user can earn (via reputation) on any Stack Exchange site.\n \nWhile
        fairly stable, over time they do change. New ones are introduced with new
        features, and the reputation requirements change as a site matures.\n \nThis
        method returns a list of privileges."
      operationId: returns-the-earnable-privileges-on-a-site-privileges-define-abilities-a-user-can-earn-via-reputation
      x-api-path-slug: privileges-get
      parameters:
      - in: query
        name: callback
        description: All API responses are JSON, we do support JSONP with the callback
          query parameter
      - in: query
        name: filter
        description: '#DiscussionThe Stack Exchange API allows applications to exclude
          almost every field returned'
      - in: query
        name: page
      - in: query
        name: pagesize
      - in: query
        name: site
        description: Each of these methods operates on a single site at a time, identified
          by the site parameter
      responses:
        200:
          description: OK
      tags:
      - Privileges
  /users/{id}/privileges:
    get:
      summary: Get User Preveleges
      description: "Returns the privileges a user has.\n \nApplications are encouraged
        to calculate privileges themselves, without repeated queries to this method.
        A simple check against the results returned by /privileges and user.user_type
        would be sufficient.\n \n{id} can contain only a single, to find it programatically
        look for user_id on user or shallow_user objects.\n \nThis method returns
        a list of privileges."
      operationId: returns-the-privileges-a-user-has-applications-are-encouraged-to-calculate-privileges-themselves-wit
      x-api-path-slug: usersidprivileges-get
      parameters:
      - in: query
        name: callback
        description: All API responses are JSON, we do support JSONP with the callback
          query parameter
      - in: query
        name: filter
        description: '#DiscussionThe Stack Exchange API allows applications to exclude
          almost every field returned'
      - in: path
        name: id
      - in: query
        name: page
      - in: query
        name: pagesize
      - in: query
        name: site
        description: Each of these methods operates on a single site at a time, identified
          by the site parameter
      responses:
        200:
          description: OK
      tags:
      - Users
      - Privileges
---