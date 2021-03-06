# Ignition GO

Ignition GO is a general purpose golang library that encapsulates a set of
common functionality for a webserver. An example webserver that utilizes
Ignition GO is [Ignition
Fuel](https://bitbucket.org/ignitionrobotics/ign-fuelserver).

Test coverage: [![codecov](https://codecov.io/bb/ignitionrobotics/ign-go/branch/default/graph/badge.svg)](https://codecov.io/bb/ignitionrobotics/ign-go)

## Environment variables

Ignition GO utilizes a set of environment variables for configuration
purposes.

1. **IGN_SSL_CERT** : Path to an SSL certificate file. This is used for local
   SSL testing and development.
1. **IGN_SSL_KEY** : Path to an SSL key. THis is used for local SSL testing and
   development
1. **IGN_DB_USERNAME** : Username for the database connection.
1. **IGN_DB_PASSWORD** : Password for the database connection.
1. **IGN_DB_ADDRESS** : URL address for the database server.
1. **IGN_DB_NAME** : Name of the database to use on the database sever.
1. **IGN_DB_MAX_OPEN_CONNS** : Max number of open connections in connections pool.
A value <= 0 means unlimited connections.
1. **IGN_GA_TRACKING_ID** : Google Analytics Tracking ID to use. If not set,
then GA will not be enabled. The format is UA-XXXX-Y.
1. **IGN_GA_APP_NAME** : Google Analytics Application Name. If not set,
then GA will not be enabled.
1. **IGN_GA_CAT_PREFIX** : (optional) A string to use as a prefix to
Google Analytics Event Category.

## Testing with Ignition GO

### Database

Ignition GO creates a separate test database to prevent data corruption.
This database is named `<DB_Name>_test`, where `<DB_Name>` is your
application's default database name which is usually equivalent to the
`IGN_DB_NAME` environment variable.
