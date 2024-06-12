# hw1
First homework for thinknetica kubernetes workshop


```bash
➜  app git:(main) ✗ kc get services
NAME                TYPE        CLUSTER-IP       EXTERNAL-IP   PORT(S)    AGE
kubernetes          ClusterIP   10.102.128.1     <none>        443/TCP    53m
rails-app-service   ClusterIP   10.102.213.127   <none>        3000/TCP   3m26s
➜  app git:(main) ✗ kc get pods
NAME                         READY   STATUS    RESTARTS   AGE
rails-app-79c8bf964c-7qbx6   1/1     Running   0          2m54s
rails-app-79c8bf964c-tx98g   1/1     Running   0          2m54s
rails-app-79c8bf964c-xxpbg   1/1     Running   0          2m54s
rails-app-79c8bf964c-zz4qt   1/1     Running   0          2m54s
➜  app git:(main) ✗ kc get deployments
NAME        READY   UP-TO-DATE   AVAILABLE   AGE
rails-app   4/4     4            4           3m
➜  app git:(main) ✗ kc logs rails-app-79c8bf964c-7qbx6
/bundle/ruby/3.3.0/gems/bootsnap-1.18.3/lib/bootsnap/load_path_cache/core_ext/kernel_require.rb:30: warning: /usr/local/lib/ruby/3.3.0/base64.rb was loaded from the standard library, but will no longer be part of the default gems since Ruby 3.4.0. Add base64 to your Gemfile or gemspec. Also contact author of activesupport-7.0.8.4 to add base64 into its gemspec.
/bundle/ruby/3.3.0/gems/bootsnap-1.18.3/lib/bootsnap/load_path_cache/core_ext/kernel_require.rb:30: warning: /usr/local/lib/ruby/3.3.0/bigdecimal.rb was loaded from the standard library, but will no longer be part of the default gems since Ruby 3.4.0. Add bigdecimal to your Gemfile or gemspec. Also contact author of activesupport-7.0.8.4 to add bigdecimal into its gemspec.
/bundle/ruby/3.3.0/gems/bootsnap-1.18.3/lib/bootsnap/load_path_cache/core_ext/kernel_require.rb:30: warning: /usr/local/lib/ruby/3.3.0/mutex_m.rb was loaded from the standard library, but will no longer be part of the default gems since Ruby 3.4.0. Add mutex_m to your Gemfile or gemspec. Also contact author of activesupport-7.0.8.4 to add mutex_m into its gemspec.
Puma starting in single mode...
* Puma version: 5.6.8 (ruby 3.3.1-p55) ("Birdie's Version")
*  Min threads: 5
*  Max threads: 5
*  Environment: development
*          PID: 1
* Listening on http://0.0.0.0:3000
Use Ctrl-C to stop
127.0.0.1 - - [12/Jun/2024:17:43:16 +0000] "GET / HTTP/1.1" 200 542 0.1501
127.0.0.1 - - [12/Jun/2024:17:43:34 +0000] "GET / HTTP/1.1" 200 542 0.0050
127.0.0.1 - - [12/Jun/2024:17:43:34 +0000] "GET / HTTP/1.1" 200 542 0.0047
127.0.0.1 - - [12/Jun/2024:17:43:35 +0000] "GET / HTTP/1.1" 200 542 0.0045
127.0.0.1 - - [12/Jun/2024:17:43:35 +0000] "GET / HTTP/1.1" 200 542 0.0041
127.0.0.1 - - [12/Jun/2024:17:43:35 +0000] "GET / HTTP/1.1" 200 542 0.0042
127.0.0.1 - - [12/Jun/2024:17:43:35 +0000] "GET / HTTP/1.1" 200 542 0.0054
127.0.0.1 - - [12/Jun/2024:17:43:35 +0000] "GET / HTTP/1.1" 200 542 0.0040
127.0.0.1 - - [12/Jun/2024:17:43:35 +0000] "GET / HTTP/1.1" 200 542 0.0040
```