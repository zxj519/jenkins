---
redirect_from:
  - /reference/commandline/pause/
description: The pause command description and usage
keywords:
- cgroups, container, suspend, SIGSTOP
title: docker pause
---

```markdown
Usage:  docker pause CONTAINER [CONTAINER...]

Pause all processes within one or more containers

Options:
      --help   Print usage
```

The `docker pause` command uses the cgroups freezer to suspend all processes in
a container. Traditionally, when suspending a process the `SIGSTOP` signal is
used, which is observable by the process being suspended. With the cgroups freezer
the process is unaware, and unable to capture, that it is being suspended,
and subsequently resumed.

See the
[cgroups freezer documentation](https://www.kernel.org/doc/Documentation/cgroup-v1/freezer-subsystem.txt)
for further details.
