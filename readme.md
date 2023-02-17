# Formatting logs in a Rust Spin application

```bash
$ spin build && spin up --listen 127.0.0.1:3001 -e RUST_LOG=logging=trace --log-dir .spin
Serving http://127.0.0.1:3001
Available Routes:
  logging: http://127.0.0.1:3001 (wildcard)

2023-02-17T11:28:25.760325Z  INFO logging: {"host": "localhost:3001", "user-agent": "curl/7.84.0", "accept": "*/*", "spin-path-info": "/", "spin-full-url": "http://localhost:3001/", "spin-matched-
route": "/...", "spin-base-path": "/", "spin-raw-component-route": "/...", "spin-component-route": ""}
```

Formatted logs are now sent to the console (this can be disabled using the `--quiet` flag), and in the `.spin` directory.
Sending logs to `stderr` or `stdout` can be configured in the tracing setup.
