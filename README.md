# Next.js Blog Site 

This is a next.js blog site I built using a [Next.js](https://nextjs.org/) guide. A version of this site (without embedded tracking) can be viewed [here](https://nextjsblog4.vercel.app/).

I recently embedded [Snowplow JavaScript trackers](https://docs.snowplowanalytics.com/docs/collecting-data/collecting-from-own-applications/javascript-trackers/browser-tracker/) to the code so that event data can be collected when you run Snowplow Micro.

## How To Use 

To run the wesbite from your computer, run this command: `npm run dev`, and go to ` https://localhost:3000/ ` in your browser.

I used Java to run [Snowplow Micro](https://github.com/snowplow-incubator/snowplow-micro/) using this command:

```java -jar snowplow-micro-1.2.1.jar --collector-config example/micro.conf --iglu example/iglu.json```

Put the collector endpoint `http://localhost:9090` into your browser, along with the following REST API endpoints to assert on the collected events:

- `/micro/all`: summary
- `/micro/good`: good events
- `/micro/bad`: bad events
- `/micro/reset`: clears cache

N.B. The wesbite [JSONLint](https://jsonlint.com/) is useful if you qucikly want to view the data in a nice format.









