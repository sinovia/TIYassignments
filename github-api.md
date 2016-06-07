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
  The recent, public activity for a specific user?

##Is there a limit to the number of requests I can make?
  Is there a way of extending that limit?
  What happens when I hit the limit?

##What if there is a lot of data returned?
  How can I ask for more (or less) data from a request?
  How do I know that there is more data available?

##What are the endpoints for fetching...
  the profile data for a user?
  the organizations a user belongs to?
  the repositories a user has created?
  a filtered list of repositories?
  a sorted list of repositories?
  public events for a user?

##When fetching public events for a user...
  How many results are returned by default?
  What limitations exist on fetching more results?
  What is the basic structure of the results?
  What fields are included in each result?
  What are the data types for each field?
  What are some of the different values for the type field?
