# Apache Airflow

## Overview

Apache Airflow is a platform to programmatically author, schedule, and monitor workflows. It is an open-source tool primarily used for orchestrating complex data pipelines. Airflow allows you to define workflows as Directed Acyclic Graphs (DAGs) of tasks, where each task represents a unit of work. You can define, schedule, and manage workflows using Python code, providing a dynamic, extensible, and scalable system.

## Core Concepts

1. **Directed Acyclic Graph (DAG):**  
   A DAG is a collection of all the tasks you want to run, organized in a way that reflects their relationships and dependencies. It defines the structure of your workflow and is scheduled and monitored by Airflow.

2. **Task:**  
   A task represents a unit of work in the workflow. Each task is an instance of an operator and is executed by a worker.

3. **Operator:**  
   Operators define individual tasks and their logic. They encapsulate the functionality needed to perform the task, such as executing Python code, running shell commands, or transferring data between systems.

4. **Task Instance:**  
   A task instance represents the execution of a task at a specific point in time. Airflow schedules tasks as task instances and keeps track of their state (e.g., success, failure).

5. **Scheduler:**  
   The scheduler is responsible for monitoring DAGs, determining when tasks should run, and executing them.

6. **Executor:**  
   The executor defines how and where task instances are run. There are several executors, such as `SequentialExecutor` (for local execution) and `CeleryExecutor` (for distributed execution).

7. **Worker:**  
   Workers are the processes that execute tasks. Depending on the executor, you can have one or many workers running in parallel.

8. **Web UI:**  
   Airflow provides a web-based UI to monitor and manage workflows. It displays DAGs, task statuses, logs, and more.

## Operators

Operators define the nature of each task and are the building blocks of workflows. Some commonly used operators include:

- **PythonOperator:**  
  Executes a Python function. It is used to run custom Python code as part of the workflow.

- **BashOperator:**  
  Executes a bash command. Useful for running shell commands or scripts.

- **PostgresOperator/MySqlOperator:**  
  Executes SQL commands in a Postgres or MySQL database. There are also operators for other databases like MSSQL, Oracle, and SQLite.

- **DummyOperator:**  
  Represents a no-op (does nothing). Useful for defining structure and dependencies in a DAG.

- **BranchPythonOperator:**  
  Allows for branching logic within a workflow. Depending on conditions, it decides which tasks downstream should be executed.

- **EmailOperator:**
  Sends an email as part of the workflow. You can use this operator to notify stakeholders about the status of a task or workflow.
