# Schema matching tools
Experimentation with existing schema matching methods

The repository contains the following:
1. Module _clustering_ with the implementation of 
[Automatic Discovery of attributes in relational database](https://www.researchgate.net/profile/Divesh_Srivastava2/publication/221213724_Automatic_Discovery_of_Attributes_in_Relational_Databases/links/55edd50108ae0af8ee19d399/Automatic-Discovery-of-Attributes-in-Relational-Databases.pdf)
2. Folder _seeping-semantics_ with scripts and guidelines on how to set up
[aurum-datadiscovery](https://github.com/mitdbg/aurum-datadiscovery)
3. Example scripts to read data for clustering and run it

## Clustering 
### column_model
The file contains the data model used in the application. 
The "Column" is a representation of a column from a database. 
To map a dataset into _Columns_, read each column of the dataset
and create a new _Column_ for each by specifying the name of the column,
the data and the source (table name). 

Next, _process_data_ is required in order to process the entire dataset
before performing any other operations. 

All of the above operations are automatically done by the main class
of the module _CorrelationClustering_

### emd_utils
The file contains the functions that computes different kinds of
Earth Mover's Distance (EMD) algorithms. 

### discovery
The file contains the main algorithms described in the paper.

### correlation_clustering
The file contains the main class of the application. 
To instantiate and work with it, the following steps must be followed:
1. Create a new _CorrelationClustering_ object 