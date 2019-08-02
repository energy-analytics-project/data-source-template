# data-source-template

This is a template repo for data sources. Please clone this repo, using a name that follows the naming convention (below) and follow the instructions.

## Naming Conventions

Data should be named like this:

	[REPO_TYPE]-[LOWERCASE_SOURCE]-[LOWERCASE_TOPIC]-[LOWERCASE_MODIFIER]

For example, the CAISO OASIS AS_REQ DAM report is named:

	data-oasis-as_req-dam

Components as in [REPO_TYPE] or [LOWERCASE_SOURCE] are separated with a dash and any internal separation in a component is with an underscore.


## Instructions

1. Replace this readme with the README_TMPLT.md filled out and renamed as README.md.
1. Update the LICENSE.md on line 189:

   Copyright [YEAR] [NAME] [COMPANY] <contact.email>
1. Build out your pipeline in ./src
1. Update the project Makefile accordingly

### Pipeline

A series of numbered scripts (python, bash, whatever) that can/will be invoked in series following the numeric order of 1 to 99. This structure allows any external orchestrator/workflow engine/script to easily execute the pipeline.

Pipelines are super simple. They do not use environment variables. Instead, they just use STDIN and STDOUT. Any shared state between steps is passed via these pipes.



### Airflow Integration

https://airflow.apache.org/installation.html

```bash
pip install apache-airflow
airflow initdb
```



### Makefile

1. Update the DATA_SOURCE_NAME on line 1 to:

	data-[LOWERCASE-SOURCE]-[LOWERCASE-TOPIC]-[LOWERCASE-MODIFIER]

## Notes

See companion project for details:

    https://github.com/energy-analytics-project/energy-dashboard
