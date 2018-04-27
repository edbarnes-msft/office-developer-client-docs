---
title: "Relations.Append Method (DAO)"
 
 
manager: soliver
ms.date: 3/9/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- dao360.chm1052904
  
localization_priority: Normal
ms.assetid: dafcc7b8-b30d-2ba2-631d-eca0f882fc2d
description: "Adds a new Relation to the Relations collection."
---

# Relations.Append Method (DAO)

Adds a new **Relation** to the **Relations** collection. 
  
## Syntax

 *expression*  . **Append**( ** *Object* ** ) 
  
 *expression*  A variable that represents a **Relations** object. 
  
### Parameters

|**Name**|**Required/Optional**|**Data Type**|**Description**|
|:-----|:-----|:-----|:-----|
| _Object_ <br/> |Required  <br/> |**Object** <br/> |An object variable that represents the field being appended to the collection.  <br/> |
   
## Remarks

The appended object becomes a persistent object, stored on disk, until you delete it by using the **Delete** method. 
  
The addition of a new object occurs immediately, but you should use the **Refresh** method on any other collections that may be affected by changes to the database structure. 
  
If the object you're appending isn't complete (such as when you haven't appended any **Field** objects to a **Fields** collection of an **Index** object before it's appended to an **Indexes** collection) or if the properties set in one or more subordinate objects are incorrect, using the **Append** method causes an error. For example, if you haven't specified a field type and then try to append the **Field** object to the **Fields** collection in a **TableDef** object, using the **Append** method triggers a run-time error. 
  
