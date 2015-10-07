https://github.com/mher/flower

A [Docker](https://www.docker.com/) container with

- celery 3
- flower

> The container should be linked to a `rabbitmq` container.

```bash
# run it

$ docker run -it --rm --link <rabbitmq container>:rabbit -p 5555:5555 emmenko/celery-flower --help
Usage: /usr/local/bin/celery [OPTIONS]

Options:

  --help                           show this help information

/usr/local/lib/python3.4/site-packages/flower/options.py options:

  --address                        run on the given address
  --auth                           regexp of emails to grant access
  --auth_provider                  auth handler class (default
                                   flower.views.auth.GoogleAuth2LoginHandler)
  --auto_refresh                   refresh dashboards (default True)
  --basic_auth                     enable http basic authentication (default
                                   [])
  --broker_api                     inspect broker e.g.
                                   http://guest:guest@localhost:15672/api/
  --ca_certs                       SSL certificate authority (CA) file
  --certfile                       SSL certificate file
  --conf                           configuration file (default flowerconfig.py)
  --cookie_secret                  secure cookie secret
  --db                             flower database file (default flower)
  --debug                          run in debug mode (default False)
  --enable_events                  periodically enable Celery events (default
                                   True)
  --format_task                    use custom task formatter
  --inspect                        inspect workers (default False)
  --inspect_timeout                inspect timeout (in milliseconds) (default
                                   1000)
  --keyfile                        SSL key file
  --max_tasks                      maximum number of tasks to keep in memory
                                   (default 10000)
  --natural_time                   show time in relative format (default True)
  --oauth2_key                     OAuth2 key (requires --auth)
  --oauth2_redirect_uri            OAuth2 redirect uri (requires --auth)
  --oauth2_secret                  OAuth2 secret (requires --auth)
  --persistent                     enable persistent mode (default False)
  --port                           run on the given port (default 5555)
  --tasks_columns                  Slugs of columns on /tasks/ page, delimited
                                   by comma (default name,uuid,state,args,kwarg
                                   s,result,received,started)
  --url_prefix                     base url prefix
  --xheaders                       enable support for the 'X-Real-Ip' and
                                   'X-Scheme' headers. (default False)

/usr/local/lib/python3.4/site-packages/tornado/log.py options:

  --log_file_max_size              max size of log files before rollover
                                   (default 100000000)
  --log_file_num_backups           number of log files to keep (default 10)
  --log_file_prefix=PATH           Path prefix for log files. Note that if you
                                   are running multiple tornado processes,
                                   log_file_prefix must be different for each
                                   of them (e.g. include the port number)
  --log_to_stderr                  Send log output to stderr (colorized if
                                   possible). By default use stderr if
                                   --log_file_prefix is not set and no other
                                   logging is configured.
  --logging=debug|info|warning|error|none
                                   Set the Python log level. If 'none', tornado
                                   won't touch the logging configuration.
                                   (default info)

```