# async
Another simple wrapper for dispatch_async

```
async { println("In the background") }
```
is equivalent to 
```
dispatch_async(dispatch_get_global_queue(qos_class_self(), 0), { println("In the background") })
```

Also: variants that specify the `dispatch_queue_t` or a `qos_class_t`, as well as a `dispatch_group_t`.
