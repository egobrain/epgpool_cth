
# epgpool common test helper
----------------------------------------------------

## Usage

```erlang
application:load(epgpool),
PgConfig = epgpool_cth:start_postgres(),
ok = epgpool_cth:set_env(PgConfig),
_ = application:ensure_all_started(epgpool),
...
ok = epgpool_cth:stop_postgres(PgConfig)
```