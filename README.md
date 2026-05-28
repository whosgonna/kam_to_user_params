Use `screen`/`tmux`. In the first pane run:

```
docker compose up -d && docker compose logs -f proxy1 proxy2
```

In a second pane run sngrep to see the traffic on the wire:
```
docker compose exec proxy1 sngrep
```

In a third pane place the test call:
```
docker compose exec uac /work/test
```
