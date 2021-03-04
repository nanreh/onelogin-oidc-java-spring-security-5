# OneLogin OpenId Connect with Spring Security 5

This repo is a copy of the [onelogin-oidc-java](https://github.com/onelogin/onelogin-oidc-java) example application provided
by OneLogin, upgraded to use the new `Spring Security 5 OAuth 2.0` implementation. The version provided by OneLogin uses
the old `Spring Security OAuth 2.x` implementation, which has been replaced in `Spring Security 5`.

This application was created using the [Spring Initializr](https://start.spring.io/) and then bits were brought over from 
the original example onelogin repo (namely, the index.html page and supporting stuff).

## Couple of notes:
1. Getting this to work was way harder than it should have been. I found the Spring documentation to be sparse and it's 
   way too easy to get incredibly mixed up trying to search for and distinguish examples made with `Spring Security OAuth 2.x` 
   from those made with the new `Spring Security 5 OAuth 2.x`. Ugly names when you need to pass them through a search engine.
2. The result is nice and simple and full of auto magic. Spring Boot does a lot of this magic these days but, again, I 
   found the documentation sparse, or maybe buried it's buried where Google's crawler didn't care to look. [This blog post](https://mycomputerninja.com/?p=818) 
   was particularly helpful. I'm posting this repo so there's at least one working example available online.

## Run Instructions
1. Read [the instructions at onelogin.com](https://developers.onelogin.com/openid-connect/connect-to-onelogin) to create 
   an OpenID Connect application.
2. Edit `application.yml` and plug in the details for the application you configured in step 1. 
3. Start the server with `./gradlew bootRun`
4. Load [http://localhost:8081/](http://localhost:8081/) in a browser. This will trigger a login with OneLogin and you 
   should see `Logged in as: Firstname Lastname` in the page.