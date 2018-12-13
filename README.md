# File Function Module



## Arch Design

![Arch](doc/design/archdesign.png)

## modules

#### common

![commonUml](doc/design/common/commonUml.png)

#### importer

![importerUml](doc/design/importer/importUml.png)

#### loader and migrationer

![loader-migrationerUml](doc/design/loaderAndMigrationer/loaderUml.png)

#### exporter

![exporterUml](doc/design/exporter/exporteUml.png)

## How to use

#### use sample

![Use Sample](doc/design/UseSample.png)

Support jdk version 1.7 or 1.7+ 

- add dependency,demo:

  ```
  <dependency>
      <groupId>com.hypers</groupId>
      <artifactId>importer</artifactId>
      <version>1.0.0</version>
  </dependency>
  ```

- add configuration in application.properties,demo:

  ```
  input_fs_dir=/tmp/input/
  parse_filename_prefixes=Task_source
  output_fs_dir=/tmp/output/
  ```

- use biz function,demo:

  ```
  val inputFsDir = dataImportJobBean.inputFsDir
  val parseFileNamePrefixes = dataImportJobBean.taskParseFileNamePrefixes
  val outputFilePath=DataImportUtils.getOutputTxtFilePath(inputFile, parseFileNamePrefixes)
  dataImportBiz.deleteOutputFile(outputFilePath)
  ```

  

