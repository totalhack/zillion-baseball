Zillion Baseball
================

This is an example repo showing how one can use
[Zillion](https://github.com/totalhack/zillion) to analyze data from the
[Baseball Data Bank](https://github.com/chadwickbureau/baseballdatabank).

The `zillion` warehouse is defined in `zillion_baseball/baseball_warehouse.json`.

To see the available warehouse metrics, dimensions, and datasources try the
following from the `zillion_warehouse` directory:

```shell
$ python warehouse.py

TODO: show output here.
```

To run reports on the command line use the `run_report.py` helper script. 

Use `--help` for more information. The output is simply a printed dataframe,
so data may be truncated in the terminal. 

> **Note:** this is meant to be a quick example. Zillion is still in its
infancy and is subject to rapid changes.