


# lib_Salesforce

Salesforce connector library. This library enables Convertigo to connect to salesforce using the SOAP protocol. 



For more technical informations : [documentation](./project.md)

- [Installation](#installation)
- [Sequences](#sequences)
    - [buildFieldsForObject](#buildfieldsforobject)
    - [createObjects](#createobjects)
    - [describeObject](#describeobject)
    - [getDeletedObjectsList](#getdeletedobjectslist)
    - [getServerTimestamp](#getservertimestamp)
    - [getUpdatedData](#getupdateddata)
    - [getUpdatedObjectsList](#getupdatedobjectslist)
    - [login](#login)
    - [loginSID](#loginsid)
    - [query](#query)
    - [queryObjectList](#queryobjectlist)
    - [readObjects](#readobjects)
    - [updateObjects](#updateobjects)
    - [upsertObjects](#upsertobjects)


## Installation

1. In your Convertigo Studio click on ![](https://github.com/convertigo/convertigo/blob/develop/eclipse-plugin-studio/icons/studio/project_import.gif?raw=true "Import a project in treeview") to import a project in the treeview
2. In the import wizard

   ![](https://github.com/convertigo/convertigo/blob/develop/eclipse-plugin-studio/tomcat/webapps/convertigo/templates/ftl/project_import_wzd.png?raw=true "Import Project")
   
   paste the text below into the `Project remote URL` field:
   <table>
     <tr><td>Usage</td><td>Click the copy button at the end of the line</td></tr>
     <tr><td>To contribute</td><td>

     ```
     lib_Salesforce=https://github.com/convertigo/c8oprj-lib-salesforce.git:branch=8.2.0
     ```
     </td></tr>
     <tr><td>To simply use</td><td>

     ```
     lib_Salesforce=https://github.com/convertigo/c8oprj-lib-salesforce/archive/8.2.0.zip
     ```
     </td></tr>
    </table>
3. Click the `Finish` button. This will automatically import the __lib_Salesforce__ project


## Sequences

### buildFieldsForObject

Utility sequence. Builds a comma separated string for all fields in a given Salesforce object. This is useful to build a Query with all fields fro a given object as SOOL is not supporting SELLECT *


**variables**

<table>
<tr>
<th>name</th><th>comment</th>
</tr>
<tr>
<td>objectType</td><td></td>
</tr>
</table>

### createObjects

Retreives object's data given a list of IDs and object Type

**variables**

<table>
<tr>
<th>name</th><th>comment</th>
</tr>
<tr>
<td>Body_create_fields</td><td></td>
</tr>
<tr>
<td>Body_create_sObjects_Id</td><td></td>
</tr>
<tr>
<td>Body_create_sObjects_type</td><td></td>
</tr>
<tr>
<td>Header_SessionHeader_sessionId</td><td></td>
</tr>
</table>

### describeObject

Describe all fields in a salesfoce for object given its type

**variables**

<table>
<tr>
<th>name</th><th>comment</th>
</tr>
<tr>
<td>objectType</td><td></td>
</tr>
</table>

### getDeletedObjectsList

Builds a list of deleted object IDs since 'delta' time stamp.  


**variables**

<table>
<tr>
<th>name</th><th>comment</th>
</tr>
<tr>
<td>delta</td><td></td>
</tr>
<tr>
<td>objectType</td><td></td>
</tr>
</table>

### getServerTimestamp

Get a salesforce based timestamp

### getUpdatedData

Builds and retrives data for objects from the list of modified objects since 'delta' timestamp.

**variables**

<table>
<tr>
<th>name</th><th>comment</th>
</tr>
<tr>
<td>__removeNamespaces</td><td></td>
</tr>
<tr>
<td>delta</td><td></td>
</tr>
<tr>
<td>objectType</td><td></td>
</tr>
</table>

### getUpdatedObjectsList

Builds a list of modified objects since 'delta' timestamp.

**variables**

<table>
<tr>
<th>name</th><th>comment</th>
</tr>
<tr>
<td>delta</td><td></td>
</tr>
<tr>
<td>objectType</td><td></td>
</tr>
</table>

### login

Login. Must be used before any other sequence. returns the Salesforce UserID or error


**variables**

<table>
<tr>
<th>name</th><th>comment</th>
</tr>
<tr>
<td>endpoint</td><td></td>
</tr>
<tr>
<td>password</td><td></td>
</tr>
<tr>
<td>username</td><td></td>
</tr>
</table>

### loginSID

Login. Must be used before any other sequence. uses a SID instead of login / password



**variables**

<table>
<tr>
<th>name</th><th>comment</th>
</tr>
<tr>
<td>apiUrl</td><td></td>
</tr>
<tr>
<td>sid</td><td></td>
</tr>
<tr>
<td>username</td><td></td>
</tr>
</table>

### query

Gets all objects and data given the objectType


**variables**

<table>
<tr>
<th>name</th><th>comment</th>
</tr>
<tr>
<td>queryString</td><td></td>
</tr>
</table>

### queryObjectList

Gets all objects and data given the objectType


**variables**

<table>
<tr>
<th>name</th><th>comment</th>
</tr>
<tr>
<td>objectType</td><td></td>
</tr>
</table>

### readObjects

Read and object from salesforce

**variables**

<table>
<tr>
<th>name</th><th>comment</th>
</tr>
<tr>
<td>ids</td><td></td>
</tr>
<tr>
<td>objectType</td><td></td>
</tr>
</table>

### updateObjects

Update an object to Salesforce

**variables**

<table>
<tr>
<th>name</th><th>comment</th>
</tr>
<tr>
<td>Body_update_sObjects_fields</td><td></td>
</tr>
<tr>
<td>Body_update_sObjects_fieldsToNull</td><td></td>
</tr>
<tr>
<td>Body_update_sObjects_Id</td><td></td>
</tr>
<tr>
<td>Body_update_sObjects_type</td><td></td>
</tr>
</table>

### upsertObjects

Insert or update and object to Salesforce

**variables**

<table>
<tr>
<th>name</th><th>comment</th>
</tr>
<tr>
<td>Body_upsert_externalIDFieldName</td><td></td>
</tr>
<tr>
<td>Body_upsert_fields</td><td></td>
</tr>
<tr>
<td>Body_upsert_sObjects_Id</td><td></td>
</tr>
<tr>
<td>Body_upsert_sObjects_type</td><td></td>
</tr>
</table>



