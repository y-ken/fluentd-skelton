# fluentd-skelton

quick test skelton for Fluentd.

## Usage

At the first time, install dependencies packages under the vendor/bundle.

```
$ bundle install --path vendor/bundle
```

execute fluentd

```
$ bundle exec fluentd --config etc/fluent.conf
```

send json to fluentd

```
$ echo '{"user":"foo"}' | bundle exec fluent-cat debug.message
```

