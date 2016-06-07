##How does the API handle authentication?
  Do I need to authenticate?

      *Authentication is strongly recommended.  There are some requests that cannot be made without authentication so.*

  What can I do with an unauthenticated request?
      *Unauthenticated clients can make 60 requests per hour.  For any more than that authentication is required*

  How can I authenticate my request? (3 ways)
      *There are three authentication methods:

        - **Basic

        - **Authentication token sent in a header:

        - **Authentication token sent in as a parameter*

##How do I ask the API for...
  The profile information for a specific user?

      *To get information on a single user, use command: GET /users/:username*

  The repository listing for a specific user?
  *To get repository listing, use command: GET /user/repos*

  The recent, public activity for a specific user?

##Is there a limit to the number of requests I can make?
  Is there a way of extending that limit?
  What happens when I hit the limit?

    *For requests using Basic Authentication or OAuth, you can make up to 5,000 requests per hour. For unauthenticated requests, the rate limit allows you to make up to 60 requests per hour.*


##What if there is a lot of data returned?
  How can I ask for more (or less) data from a request?
  How do I know that there is more data available?

##What are the endpoints for fetching...
  the profile data for a user?
    *"html_url":*

  the organizations a user belongs to?
    *"organizations_url"*

  the repositories a user has created?
    *"repos_url"*

  a filtered list of repositories?
    *d*

  a sorted list of repositories?
    *d*

  public events for a user?
    *"events_url":*

##When fetching public events for a user...
  How many results are returned by default?
    *Activity from the past 90 days*

  What limitations exist on fetching more results?
    *Unauthenticated users can only see public results.  Authenticated users can also see private results.*

  What is the basic structure of the results?
  *Status: 200 OK
Link: <https://api.github.com/resource?page=2>; rel="next",
      <https://api.github.com/resource?page=5>; rel="last"
X-RateLimit-Limit: 5000
X-RateLimit-Remaining: 4999
[
  {
    "type": "Event",
    "public": true,
    "payload": {
    },
    "repo": {
      "id": 3,
      "name": "octocat/Hello-World",
      "url": "https://api.github.com/repos/octocat/Hello-World"
    },
    "actor": {
      "id": 1,
      "login": "octocat",
      "gravatar_id": "",
      "avatar_url": "https://github.com/images/error/octocat_happy.gif",
      "url": "https://api.github.com/users/octocat"
    },
    "org": {
      "id": 1,
      "login": "github",
      "gravatar_id": "",
      "url": "https://api.github.com/orgs/github",
      "avatar_url": "https://github.com/images/error/octocat_happy.gif"
    },
    "created_at": "2011-09-06T17:26:27Z",
    "id": "12345"
  }
