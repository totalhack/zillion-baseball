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

"""
---- Warehouse
metrics:
  {
      'at_bats': <Metric name='at_bats' type='integer'>,
      'batting_average': <FormulaMetric name='batting_average'
formula='1.0*{hits}/{at_bats}' aggregation='mean' technical=None>,
      'caught_stealing': <Metric name='caught_stealing' type='integer'>,
      'doubles': <Metric name='doubles' type='integer'>,
      'games': <Metric name='games' type='integer'>,
      ...
"""
```

To run reports on the command line use the `run_report.py` helper script. 

```shell
$ python run_report.py -m hits home_runs -d franchise_name -c '[("year", "=", "2018")]'

"""
                                  H   HR
Franchise Name                          
Arizona Diamondbacks           1283  176
Atlanta Braves                 1433  175
Baltimore Orioles              1317  188
Boston Red Sox                 1509  208
Chicago Cubs                   1453  167
Chicago White Sox              1332  182
...
"""
```

Use `--help` for more information. The output is simply a printed dataframe,
so data may be truncated in the terminal. 

> **Note:** this is meant to be a quick example. Zillion is still in its
infancy and is subject to rapid changes.