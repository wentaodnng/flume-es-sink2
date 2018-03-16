
# EsSink2

This is Flume-NG Sink for Elasticsearch = 2.3.*
I developed this because the official version does not support Elasticsearch 2.3.* due to API changes.


# Requirements

- Flume-NG = 1.8
- Elasticsearch = 2.3.*

# Build


Build fat jar which contains elasticsearch dependencies
```bash
$ gradle assembly
```

Jar will be generated in `build/libs`


# Usage

1. Append the built jar to Flume's classpath
2. remove `guava-*.jar` and `jackson-core-*.jar` in flume's default libs dir. They are outdated and newer version are included in Elasticsearch.
3. set sink type to `com.dwt.flume.sink.elasticsearch2.ElasticSearchSink` in flume.conf
4. start flume agent
