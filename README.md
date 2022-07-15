# api_load_testing_tool - written in Golang

```
the repo consis of some example & demonstarted how to use the benchmark tool/function
it sends conecurrent request repeatedly for multiple time, each batch may have 1000 conecurrent request,
here demonstrated benchmark on
1. sign up (dynamic input, stores the dynamically generated payload locally)
2. login (login with stored credential from above, then intercept response to collect cookie & csrf tokens)
3. get user info (interecpt request to attach same cookie & csrf tokens)
4. get the multiple user info with pagination (here all user can see all user - like all user is admin, data just for demonstration)
```

## tool to run benchmark on API
### like apache benchmark, its support to set total request to send & level of concurrency for the each bulk requests
### allows user to feed dynamic input payload like, username, password
### allow user to benchmark multiple API in the single script
### in a script user can call benchmark api multiple type & paralley, user can collect data from one API & use the extracted data to next API
### allows user to intercept request & response, example usage is to intercept response to collect cookie and then intercept next request to attach cookie
### for now the data is collected in API, have plan to show summarised graphical data like charts of live update
