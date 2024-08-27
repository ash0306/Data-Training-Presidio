# Azure - DataFactory

Got started on Azure DataFactory.

## Topics Explored
### 1. Pipelines
A **pipeline** in Azure Data Factory (ADF) is a logical grouping of activities that perform a specific task. A pipeline allows you to manage the activities as a set instead of each one individually. For example, you might have a pipeline that runs several tasks in a sequence, such as copying data from a source to a destination, transforming the data, and then loading it into a data warehouse.

**Key Features:**
- **Activities**: These are the steps that make up the pipeline. They can include data movement, data transformation, and control activities.
- **Triggers**: Pipelines can be triggered manually, on a schedule, or by events.

### 2. Copy Activity
The **Copy Activity** in Azure Data Factory is used to copy data from one location to another. It’s one of the most commonly used activities in ADF and can move data between various types of data stores, such as databases, file systems, and cloud storage services.

**Key Features:**
- **Source and Destination**: Define where the data is coming from and where it is going.
- **Mapping**: Map columns from the source to the destination.
- **Performance Optimization**: Options to configure parallelism and fault tolerance.

### 3. Expression Builder
The **Expression Builder** in Azure Data Factory allows you to create dynamic expressions for use within activities. These expressions can manipulate string values, perform mathematical operations, and control the flow of the pipeline based on conditions.

**Key Features:**
- **Variables and Functions**: Use system variables and built-in functions to create dynamic content.
- **Parameters**: Reference pipeline parameters and dataset properties within expressions.

### 4. Difference Between Variable and Parameter
- **Variables**: 
  - Variables in ADF are used to store temporary values that can be used within the pipeline. 
  - They can be updated during the execution of a pipeline and are specific to the pipeline instance.
  - **Example**: You might use a variable to count the number of rows processed or to store an intermediate result.

- **Parameters**: 
  - Parameters are used to pass values into a pipeline, activity, or data set at the time of execution.
  - They are defined when you create the pipeline or activity and cannot be changed during execution.
  - **Example**: You might use a parameter to pass the file path of the data you want to process or the date range for a data load.

### 5. What is Bulk Insert?
**Bulk Insert** is a technique used to insert a large volume of data into a database efficiently. In Azure Data Factory, when performing data loading operations, bulk insert can be used to improve performance by reducing the number of individual insert operations.

**Key Features:**
- **High Performance**: Bulk insert operations can load data much faster than inserting rows individually.
- **Use Case**: Ideal for scenarios where you need to load millions of rows into a table.

