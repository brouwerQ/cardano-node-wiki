This page describes the benchmarking procedure.

## Bench Deployer Access

First of all, please make sure you have access to the `bench-deployer` server by typing this command on your computer:

```
$ ssh bench
```

You will be logged in as `dev@bench-deployer`.

## `cardano-ops` Repository

Also, please make sure you have access to [cardano-ops](https://github.com/input-output-hk/cardano-ops) repository. You need it to be able to push in our branch `bench-master`.

## Benchmarking Profiles

Each benchmark has a **profile**. The profile is a set of parameters that specify its particular details.

Clone `cardano-ops` repository, go to it, switch to `bench-master` branch and find `bench/profile-definitions.jq` file. This file describes existing profiles, we'll explore it later.

## Working on Bench Deployer

Now log in to `bench-deployer` server using `ssh bench` command.

**IMPORTANT**: Please remember that all actions on `bench-deployer` server must always be performed in `screen` emulation. So first of all, run `screen -x` command.

There are important `screen`-windows we need:

1. `bench-0` - for running benchmarks on **small** clusters.
2. `bench-1` - for running benchmarks on **big** (real-world) clusters.
3. `bench-2` - for running benchmarks on **small** clusters.
4. `workbench-1` - for running **analyzing** of benchmarks results.

To move between `screen`-windows, use following key combinations: `(Ctrl+A)+P` (to the right) or `(Ctrl+A)+N` (to the left).

**IMPORTANT**: do not use `exit` command in the `screen`-window! Instead, just close your terminal window, to keep `screen`-window working.