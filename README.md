# Docker Sauce Labs Connect

This docker image runs [Sauce Labs Connect](https://docs.saucelabs.com/reference/sauce-connect/) on Java 8.

## Usage

It sets the `sc` CLI as the entrypoint so it can be used as a replacement via
an shell alias:

```sh
$ alias sc="sudo docker run --rm -it -p 8000:8000 jordan/sauce-connect"
$ sc -P 8000 -u $SAUCE_USERNAME -k SAUCE_ACCESS_KEY
```

Or just

```sh
$ sudo docker run -rm -it \
             -p 0.0.0.0:8000:8000 \
             jordan/sauce-connect -P 8000 \
                                        -u $SAUCE_USERNAME \
                                        -k $SAUCE_ACCESS_KEY \
                                        --tunnel-identifier foo
```


## Useful links
1. [Sauce Connect Command Line Reference](https://wiki.saucelabs.com/pages/viewpage.action?pageId=48365781)
