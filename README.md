# rama-demo-gallery

This repository contains a collection of short, self-contained, thoroughly commented examples of applying [Rama](https://redplanetlabs.com) towards a variety of use cases. All of these examples can scale to millions of reads and writes per second. Without Rama, these examples would require using and operating multiple pieces of specialized infrastructure. Each example has identical Java and Clojure implementations to demonstrate the Java API and Clojure API respectively. The examples are:

- **ProfileModule**: Implements account registration, profiles, and profile editing. [Java implementation](src/main/java/rama/gallery/profiles/ProfileModule.java) and [Clojure implementation](src/main/clj/rama/gallery/profile_module.clj). See the [Java tests](src/test/java/rama/gallery/ProfileModuleTest.java) or [Clojure tests](src/test/clj/rama/gallery/profile_module_test.clj) for how to interact with this module to register accounts, edit profiles, and query for profile data.
- **TimeSeriesModule**: Implements time-series analytics for latencies of rendering URLs on a website. [Java implementation](src/main/java/rama/gallery/timeseries/TimeSeriesModule.java) and [Clojure implementation](src/main/clj/rama/gallery/time_series_module.clj). Aggregates an index of min/max/average statistics for minute, hour, day, and monthly granularities. See the [Java tests](src/test/java/rama/gallery/TimeSeriesModuleTest.java) or [Clojure tests](src/test/clj/rama/gallery/time_series_module_test.clj) for how clients perform various kinds of range queries on this index.
- **TopUsersModule**: Implements top-N analytics on user activity in the context of an e-commerce site. [Java implementation](src/main/java/rama/gallery/topusers/TopUsersModule.java) and [Clojure implementation](src/main/clj/rama/gallery/top_users_module.clj). It tracks in realtime the top 500 users who have spent the most money on the service. See the [Java tests](src/test/java/rama/gallery/TopUsersModuleTest.java) or [Clojure tests](src/test/clj/rama/gallery/top_users_module_test.clj) for examples of querying the module.



## Running tests

Java tests can be run with `mvn test`, or a specific test class can be run like `mvn test -Dtest=ProfileModuleTest`.

Clojure tests can be run with `lein test`. 
