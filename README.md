# fluentd-skelton

quick test skelton for Fluentd.

## Usage

At the first time, install dependencies packages under the vendor/bundle.

```
$ bundle install --path vendor/bundle
```

install fluent-plugin

```
# add line to Gemfile
$ echo "gem "fluent-plugin-rewrite-tag-filter"" >> Gemfile

# install them
$ bundle install
```

execute fluentd

```
# verbose mode
$ bundle exec fluentd --config etc/fluent.conf

# background mode
$ bundle exec fluentd --config etc/fluent.conf --log fluent.log &
```

send json to fluentd

```
$ echo '{"user":"foo"}' | bundle exec fluent-cat debug.message
```

