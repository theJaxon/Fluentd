# Fluentd

### Directives

| Directive |                                     Description                                    |
|:---------:|:----------------------------------------------------------------------------------:|
|   source  |                     Tells fluentd to receive/source log events                     |
|   match   |                        Match log events to other operations (Output)               |
|   filter  | Controls which events are handled by 1 or more processes (referred to as pipeline) |
|  @include |         Bring in other config files (Just like import in conventional code)        |
|   label   |                    Provides a grouping mechanism for log events                    |
|   system  |           related to fluentd internal configs (ex: setting of log levels)          |

---

### hello-world config usage
```bash
# Receive log events from port 18080
fluentd -c hello-world.conf

# Generating an event
curl -H "Content-type: application/json" -d '{"Hello": "World"}' 'localhost:18080'
```

### Validating config files
```bash
fluentd -c <conf> --dry-run
```

---