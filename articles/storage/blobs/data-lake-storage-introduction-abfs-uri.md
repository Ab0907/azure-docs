---
title: Use the Azure Data Lake Storage Gen2 URI
description: Learn URI syntax for the abfs scheme identifier, which represents the Azure Blob File System driver (Hadoop Filesystem driver for Azure Data Lake Storage Gen2).
author: normesta
ms.topic: conceptual
ms.author: normesta
ms.date: 12/06/2018
ms.service: storage
ms.subservice: data-lake-storage-gen2
ms.reviewer: jamesbak
---

# Use the Azure Data Lake Storage Gen2 URI

The [Hadoop Filesystem](https://www.aosabook.org/en/hdfs.html) driver that is compatible with Azure Data Lake Storage Gen2 is known by its scheme identifier `abfs` (Azure Blob File System). Consistent with other Hadoop Filesystem drivers, the ABFS driver employs a URI format to address files and directories within a Data Lake Storage Gen2 capable account.

## URI syntax

The URI syntax for Data Lake Storage Gen2 is dependent on whether or not your storage account is set up to have Data Lake Storage Gen2 as the default file system.

If the Data Lake Storage Gen2 capable account you wish to address **is not** set as the default file system during account creation, then the shorthand URI syntax is:

<pre>abfs[s]<sup>1</sup>://&lt;file_system&gt;<sup>2</sup>@&lt;account_name&gt;<sup>3</sup>.dfs.core.windows.net/&lt;path&gt;<sup>4</sup>/&lt;file_name&gt;<sup>5</sup></pre>

1. **Scheme identifier**: The `abfs` protocol is used as the scheme identifier. If you add an 's' at the end (abfs<b><i>s</i></b>) then the ABFS Hadoop client driver will <i>ALWAYS</i> use Transport Layer Security (TLS) irrespective of the authentication method chosen. If you choose OAuth as your authentication then the client driver will always use TLS even if you specify 'abfs' instead of 'abfss' because OAuth solely relies on the TLS layer. Finally, if you choose to use the older method of storage account key, then the client driver will interpret 'abfs' to mean that you do not want to use TLS.

2. **File system**: The parent location that holds the files and folders. This is the same as Containers in the Azure Storage Blobs service.

3. **Account name**: The name given to your storage account during creation.

4. **Paths**: A forward slash delimited (`/`) representation of the directory structure.

5. **File name**: The name of the individual file. This parameter is optional if you are addressing a directory.

However, if the account you wish to address is set as the default file system during account creation, then the shorthand URI syntax is:

<pre>/&lt;path&gt;<sup>1</sup>/&lt;file_name&gt;<sup>2</sup></pre>

1. **Path**: A forward slash delimited (`/`) representation of the directory structure.

2. **File Name**: The name of the individual file.

## Next steps

- [Use Azure Data Lake Storage Gen2 with Azure HDInsight clusters](../../hdinsight/hdinsight-hadoop-use-data-lake-storage-gen2.md?toc=%2fazure%2fstorage%2fblobs%2ftoc.json)
