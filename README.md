<!--
 ___ _            _ _    _ _    __
/ __(_)_ __  _ __| (_)__(_) |_ /_/
\__ \ | '  \| '_ \ | / _| |  _/ -_)
|___/_|_|_|_| .__/_|_\__|_|\__\___|
            |_| 
-->
![](https://docs.simplicite.io//logos/logo250.png)
* * *

`Crm` module definition
=======================



`CrmAccSector` business object definition
-----------------------------------------



### Fields

| Name                                                         | Type                                     | Required | Updatable | Personal | Description                                                                      |
|--------------------------------------------------------------|------------------------------------------|----------|-----------|----------|----------------------------------------------------------------------------------|
| `crmSecSector`                                               | char(255)                                | yes*     | yes       |          | -                                                                                |

`CrmCollaborator` business object definition
--------------------------------------------



### Fields

| Name                                                         | Type                                     | Required | Updatable | Personal | Description                                                                      |
|--------------------------------------------------------------|------------------------------------------|----------|-----------|----------|----------------------------------------------------------------------------------|

### Custom actions

* `resetPassword`: 

`CrmSource` business object definition
--------------------------------------



### Fields

| Name                                                         | Type                                     | Required | Updatable | Personal | Description                                                                      |
|--------------------------------------------------------------|------------------------------------------|----------|-----------|----------|----------------------------------------------------------------------------------|
| `crmSrcLabel`                                                | char(255)                                | yes*     | yes       |          | -                                                                                |

`CrmActType` business object definition
---------------------------------------



### Fields

| Name                                                         | Type                                     | Required | Updatable | Personal | Description                                                                      |
|--------------------------------------------------------------|------------------------------------------|----------|-----------|----------|----------------------------------------------------------------------------------|
| `crmActTypeLabel`                                            | char(255)                                | yes*     | yes       |          | -                                                                                |

`CrmCompetitor` business object definition
------------------------------------------



### Fields

| Name                                                         | Type                                     | Required | Updatable | Personal | Description                                                                      |
|--------------------------------------------------------------|------------------------------------------|----------|-----------|----------|----------------------------------------------------------------------------------|
| `crmCompName`                                                | char(50)                                 | yes*     | yes       |          | -                                                                                |
| `crmCompComment`                                             | text(1000)                               |          | yes       |          | -                                                                                |
| `crmCompDocuments`                                           | document                                 |          | yes       |          | -                                                                                |

`CrmAccount` business object definition
---------------------------------------



### Fields

| Name                                                         | Type                                     | Required | Updatable | Personal | Description                                                                      |
|--------------------------------------------------------------|------------------------------------------|----------|-----------|----------|----------------------------------------------------------------------------------|
| `crmAccName`                                                 | char(255)                                | yes*     | yes       |          | -                                                                                |
| `crmAccEmployee`                                             | int(10)                                  |          | yes       |          | -                                                                                |
| `crmAccComment`                                              | text(1500)                               |          | yes       |          | -                                                                                |
| `crmAccShortLabel`                                           | char(10)                                 |          | yes       |          | -                                                                                |
| `crmAccTurnover`                                             | int(11)                                  |          | yes       |          | -                                                                                |
| `crmAccSecId` link to **`CrmAccSector`**                     | id                                       |          | yes       |          | -                                                                                |
| _Ref. `crmAccSecId.crmSecSector`_                            | _char(255)_                              |          |           |          | -                                                                                |
| `crmAccStreet`                                               | char(255)                                |          | yes       |          | -                                                                                |
| `crmAccPostalcode`                                           | int(5)                                   |          | yes       |          | -                                                                                |
| `crmAccCity`                                                 | char(255)                                |          | yes       |          | -                                                                                |
| `crmAccCountry`                                              | char(255)                                |          | yes       |          | -                                                                                |
| `crmAccWebsite`                                              | url(255)                                 |          | yes       |          | -                                                                                |
| `crmAccPhone`                                                | phone(100)                               |          | yes       |          | -                                                                                |
| `crmAccId` link to **`CrmAccount`**                          | id                                       |          | yes       |          | -                                                                                |
| _Ref. `crmAccId.crmAccName`_                                 | _char(255)_                              |          |           |          | -                                                                                |
| _Ref. `crmAccId.crmAccComment`_                              | _text(1500)_                             |          |           |          | -                                                                                |
| _Ref. `crmAccId.crmAccShortLabel`_                           | _char(10)_                               |          |           |          | -                                                                                |
| `crmAccColId` link to **`CrmCollaborator`**                  | id                                       |          | yes       |          | -                                                                                |
| _Ref. `crmAccColId.usr_login`_                               | _regexp(100)_                            |          |           | yes      | _Login_                                                                          |
| `crmAccDocuments`                                            | document                                 |          | yes       |          | -                                                                                |

`CrmContact` business object definition
---------------------------------------



### Fields

| Name                                                         | Type                                     | Required | Updatable | Personal | Description                                                                      |
|--------------------------------------------------------------|------------------------------------------|----------|-----------|----------|----------------------------------------------------------------------------------|
| `crmCtcName`                                                 | char(30)                                 | yes*     | yes       |          | -                                                                                |
| `crmCtcFirstName`                                            | char(40)                                 | yes*     | yes       |          | -                                                                                |
| `crmCtcAccId` link to **`CrmAccount`**                       | id                                       |          | yes       |          | -                                                                                |
| _Ref. `crmCtcAccId.crmAccName`_                              | _char(255)_                              |          |           |          | -                                                                                |
| `crmCtcColId` link to **`CrmCollaborator`**                  | id                                       |          | yes       |          | -                                                                                |
| _Ref. `crmCtcColId.usr_login`_                               | _regexp(100)_                            |          |           | yes      | _Login_                                                                          |
| `crmCtcEmail`                                                | email(100)                               |          | yes       |          | -                                                                                |
| `crmCtcPhone`                                                | phone(100)                               |          | yes       |          | -                                                                                |
| `crmCtcMobile`                                               | phone(100)                               |          | yes       |          | -                                                                                |
| `crmCtcComment`                                              | text(1500)                               |          | yes       |          | -                                                                                |
| `crmCtcFunction`                                             | char(255)                                |          | yes       |          | -                                                                                |
| `crmCtcAddress`                                              | char(255)                                |          | yes       |          | -                                                                                |
| `crmCtcPostalcode`                                           | int(5)                                   |          | yes       |          | -                                                                                |
| `crmCtcCity`                                                 | char(255)                                |          | yes       |          | -                                                                                |
| `crmCtcWebsite`                                              | url(100)                                 |          | yes       |          | -                                                                                |
| `crmCtcId` link to **`CrmContact`**                          | id                                       |          | yes       |          | -                                                                                |
| _Ref. `crmCtcId.crmCtcName`_                                 | _char(30)_                               |          |           |          | -                                                                                |
| _Ref. `crmCtcId.crmCtcFirstName`_                            | _char(40)_                               |          |           |          | -                                                                                |
| _Ref. `crmCtcId.crmCtcComment`_                              | _text(1500)_                             |          |           |          | -                                                                                |
| _Ref. `crmCtcId.crmCtcFunction`_                             | _char(255)_                              |          |           |          | -                                                                                |
| _Ref. `crmCtcId.crmCtcComment`_                              | _text(1500)_                             |          |           |          | -                                                                                |
| `crmCtcSrcId` link to **`CrmSource`**                        | id                                       |          | yes       |          | -                                                                                |
| _Ref. `crmCtcSrcId.crmSrcLabel`_                             | _char(255)_                              |          |           |          | -                                                                                |

`CrmContactHistoric` business object definition
-----------------------------------------------



### Fields

| Name                                                         | Type                                     | Required | Updatable | Personal | Description                                                                      |
|--------------------------------------------------------------|------------------------------------------|----------|-----------|----------|----------------------------------------------------------------------------------|
| `row_ref_id` link to **`CrmContact`**                        | id                                       | yes*     |           |          | Record row ID                                                                    |
| `row_idx`                                                    | int(11)                                  | yes*     | yes       |          | History record index                                                             |
| `created_by_hist`                                            | char(100)                                | yes*     |           |          | Created by                                                                       |
| `created_dt_hist`                                            | datetime                                 | yes*     |           |          | Created date                                                                     |
| `crmCtcName`                                                 | char(30)                                 | yes*     | yes       |          | -                                                                                |
| `crmCtcFirstName`                                            | char(40)                                 | yes*     | yes       |          | -                                                                                |
| `crmCtcAccId` link to **`CrmAccount`**                       | id                                       |          | yes       |          | -                                                                                |
| _Ref. `crmCtcAccId.crmAccName`_                              | _char(255)_                              |          |           |          | -                                                                                |
| `crmCtcColId` link to **`CrmCollaborator`**                  | id                                       |          | yes       |          | -                                                                                |
| _Ref. `crmCtcColId.usr_login`_                               | _regexp(100)_                            |          |           | yes      | _Login_                                                                          |

`CrmLead` business object definition
------------------------------------



### Fields

| Name                                                         | Type                                     | Required | Updatable | Personal | Description                                                                      |
|--------------------------------------------------------------|------------------------------------------|----------|-----------|----------|----------------------------------------------------------------------------------|
| `crmLeadCreation`                                            | date                                     | yes      | yes       |          | -                                                                                |
| `crmLeadTitle`                                               | char(255)                                | yes      | yes       |          | -                                                                                |
| `crmLeadState`                                               | enum(15) using `CRMLEADSTATE` list       | yes      | yes       |          | -                                                                                |
| `crmLeadDocuments`                                           | document                                 |          | yes       |          | -                                                                                |
| `crmLeadDescription`                                         | text(2000)                               |          | yes       |          | -                                                                                |
| `crmLeadCtcId` link to **`CrmContact`**                      | id                                       | yes      | yes       |          | -                                                                                |
| _Ref. `crmLeadCtcId.crmCtcFirstName`_                        | _char(40)_                               |          |           |          | -                                                                                |
| _Ref. `crmLeadCtcId.crmCtcName`_                             | _char(30)_                               |          |           |          | -                                                                                |
| _Ref. `crmLeadCtcId.crmCtcFunction`_                         | _char(255)_                              |          |           |          | -                                                                                |
| _Ref. `crmLeadCtcId.crmCtcMobile`_                           | _phone(100)_                             |          |           |          | -                                                                                |
| _Ref. `crmLeadCtcId.crmCtcEmail`_                            | _email(100)_                             |          |           |          | -                                                                                |
| `crmLeadAccId` link to **`CrmAccount`**                      | id                                       |          | yes       |          | -                                                                                |
| _Ref. `crmLeadAccId.crmAccName`_                             | _char(255)_                              |          |           |          | -                                                                                |
| _Ref. `crmLeadAccId.crmAccComment`_                          | _text(1500)_                             |          |           |          | -                                                                                |
| _Ref. `crmLeadAccId.crmAccSecId`_                            | _id_                                     |          |           |          | -                                                                                |
| _Ref. `crmAccSecId.crmSecSector`_                            | _char(255)_                              |          |           |          | -                                                                                |
| _Ref. `crmLeadAccId.crmAccColId`_                            | _id_                                     |          |           |          | -                                                                                |
| _Ref. `crmAccColId.usr_login`_                               | _regexp(100)_                            |          |           | yes      | _Login_                                                                          |
| `crmLeadColId` link to **`CrmCollaborator`**                 | id                                       |          | yes       |          | -                                                                                |
| _Ref. `crmLeadColId.usr_login`_                              | _regexp(100)_                            |          |           | yes      | _Login_                                                                          |
| `crmLeadSrcId` link to **`CrmSource`**                       | id                                       |          | yes       |          | -                                                                                |
| _Ref. `crmLeadSrcId.crmSrcLabel`_                            | _char(255)_                              |          |           |          | -                                                                                |

### Lists

* `CRMLEADSTATE`
    - `TBQ` To be qualified
    - `OK` OK
    - `KO` KO

`CrmOpportunity` business object definition
-------------------------------------------



### Fields

| Name                                                         | Type                                     | Required | Updatable | Personal | Description                                                                      |
|--------------------------------------------------------------|------------------------------------------|----------|-----------|----------|----------------------------------------------------------------------------------|
| `crmOppTitle`                                                | char(255)                                | yes*     | yes       |          | -                                                                                |
| `crmOppState`                                                | enum(30) using `CRM_OPP_STATE` list      | yes      | yes       |          | -                                                                                |
| `crmOppAmount`                                               | float(11, 2)                             |          |           |          | -                                                                                |
| `crmOppEstimatedAmount`                                      | float(10, 2)                             |          |           |          | -                                                                                |
| `crmOppColId` link to **`CrmCollaborator`**                  | id                                       |          | yes       |          | -                                                                                |
| _Ref. `crmOppColId.usr_login`_                               | _regexp(100)_                            |          |           | yes      | _Login_                                                                          |
| _Ref. `crmOppColId.usr_first_name`_                          | _char(50)_                               |          |           | yes      | _First name_                                                                     |
| _Ref. `crmOppColId.usr_last_name`_                           | _char(50)_                               |          |           | yes      | _Last name_                                                                      |
| `crmOppLeadId` link to **`CrmLead`**                         | id                                       |          | yes       |          | -                                                                                |
| _Ref. `crmOppLeadId.crmLeadCreation`_                        | _date_                                   |          |           |          | -                                                                                |
| `crmOppDocuments`                                            | document                                 |          | yes       |          | -                                                                                |
| _Ref. `crmOppLeadId.crmLeadTitle`_                           | _char(255)_                              |          |           |          | -                                                                                |
| _Ref. `crmOppLeadId.crmLeadCtcId`_                           | _id_                                     |          |           |          | -                                                                                |
| _Ref. `crmLeadCtcId.crmCtcFirstName`_                        | _char(40)_                               |          |           |          | -                                                                                |
| _Ref. `crmLeadCtcId.crmCtcName`_                             | _char(30)_                               |          |           |          | -                                                                                |
| _Ref. `crmLeadCtcId.crmCtcMobile`_                           | _phone(100)_                             |          |           |          | -                                                                                |
| _Ref. `crmLeadCtcId.crmCtcEmail`_                            | _email(100)_                             |          |           |          | -                                                                                |
| _Ref. `crmLeadCtcId.crmCtcFunction`_                         | _char(255)_                              |          |           |          | -                                                                                |
| `crmOppAccId` link to **`CrmAccount`**                       | id                                       |          | yes       |          | -                                                                                |
| _Ref. `crmOppAccId.crmAccName`_                              | _char(255)_                              |          |           |          | -                                                                                |
| _Ref. `crmOppAccId.crmAccComment`_                           | _text(1500)_                             |          |           |          | -                                                                                |
| _Ref. `crmOppLeadId.crmLeadAccId`_                           | _id_                                     |          |           |          | -                                                                                |
| _Ref. `crmLeadAccId.crmAccComment`_                          | _text(1500)_                             |          |           |          | -                                                                                |
| _Ref. `crmLeadAccId.crmAccName`_                             | _char(255)_                              |          |           |          | -                                                                                |
| _Ref. `crmLeadAccId.crmAccSecId`_                            | _id_                                     |          |           |          | -                                                                                |
| _Ref. `crmOppLeadId.crmLeadColId`_                           | _id_                                     |          |           |          | -                                                                                |
| _Ref. `crmLeadColId.usr_login`_                              | _regexp(100)_                            |          |           | yes      | _Login_                                                                          |
| `crmOppComment`                                              | text(2000)                               |          | yes       |          | -                                                                                |
| _Ref. `crmAccSecId.crmSecSector`_                            | _char(255)_                              |          |           |          | -                                                                                |

### Lists

* `CRM_OPP_STATE`
    - `DR` Draft
    - `PR` Prospection
    - `QU` Qualification
    - `OF` Offer
    - `NE` Negociation
    - `W` Won
    - `LO` Lost
    - `AB` Abandonned

`CrmActivity` business object definition
----------------------------------------



### Fields

| Name                                                         | Type                                     | Required | Updatable | Personal | Description                                                                      |
|--------------------------------------------------------------|------------------------------------------|----------|-----------|----------|----------------------------------------------------------------------------------|
| `crmActId`                                                   | int(11)                                  | yes*     | yes       |          | -                                                                                |
| `crmActWhen`                                                 | datetime                                 | yes      | yes       |          | -                                                                                |
| `crmActTitle`                                                | char(255)                                | yes      | yes       |          | -                                                                                |
| `crmActDocuments`                                            | document                                 |          | yes       |          | -                                                                                |
| `crmActivityCrmActTypefk` link to **`CrmActType`**           | id                                       |          | yes       |          | -                                                                                |
| _Ref. `crmActivityCrmActTypefk.crmActTypeLabel`_             | _char(255)_                              |          |           |          | -                                                                                |
| `crmActDescription`                                          | text(2000)                               |          | yes       |          | -                                                                                |
| `crmAccAct` link to **`CrmAccount`**                         | id                                       |          | yes       |          | -                                                                                |
| `crmActOppId` link to **`CrmOpportunity`**                   | id                                       |          | yes       |          | -                                                                                |
| _Ref. `crmActOppId.crmOppTitle`_                             | _char(255)_                              |          |           |          | -                                                                                |
| _Ref. `crmActOppId.crmOppState`_                             | _enum(30) using `CRM_OPP_STATE` list_    |          |           |          | -                                                                                |
| _Ref. `crmActOppId.crmOppColId`_                             | _id_                                     |          |           |          | -                                                                                |
| _Ref. `crmOppColId.usr_login`_                               | _regexp(100)_                            |          |           | yes      | _Login_                                                                          |
| _Ref. `crmActOppId.crmOppAccId`_                             | _id_                                     |          |           |          | -                                                                                |
| _Ref. `crmOppAccId.crmAccName`_                              | _char(255)_                              |          |           |          | -                                                                                |

### Lists

* `CRM_OPP_STATE`
    - `DR` Draft
    - `PR` Prospection
    - `QU` Qualification
    - `OF` Offer
    - `NE` Negociation
    - `W` Won
    - `LO` Lost
    - `AB` Abandonned

`CrmProduct` business object definition
---------------------------------------



### Fields

| Name                                                         | Type                                     | Required | Updatable | Personal | Description                                                                      |
|--------------------------------------------------------------|------------------------------------------|----------|-----------|----------|----------------------------------------------------------------------------------|
| `crmPrdLabel`                                                | char(30)                                 | yes*     | yes       |          | -                                                                                |
| `crmPrdPrice`                                                | float(11, 2)                             | yes      | yes       |          | -                                                                                |
| `crmPrdDocuments`                                            | document                                 |          | yes       |          | -                                                                                |
| `crmPrdBillingMethod`                                        | enum(255) using `CRMPRDBILLINGMETHOD` list |          | yes       |          | -                                                                                |
| `crmPrdReference`                                            | char(255)                                |          | yes       |          | -                                                                                |

### Lists

* `CRMPRDBILLINGMETHOD`
    - `Unitary` UNI
    - `Daily` DAY
    - `Weekly` WEE
    - `Monthly` MON
    - `Yearly` YEA

`CrmCtcAct` business object definition
--------------------------------------



### Fields

| Name                                                         | Type                                     | Required | Updatable | Personal | Description                                                                      |
|--------------------------------------------------------------|------------------------------------------|----------|-----------|----------|----------------------------------------------------------------------------------|
| `crmCtcactCtcId` link to **`CrmContact`**                    | id                                       | yes*     | yes       |          | -                                                                                |
| _Ref. `crmCtcactCtcId.crmCtcName`_                           | _char(30)_                               |          |           |          | -                                                                                |
| _Ref. `crmCtcactCtcId.crmCtcFirstName`_                      | _char(40)_                               |          |           |          | -                                                                                |
| `crmCtcactActId` link to **`CrmActivity`**                   | id                                       | yes*     | yes       |          | -                                                                                |
| _Ref. `crmCtcactActId.crmActId`_                             | _int(11)_                                |          |           |          | -                                                                                |
| _Ref. `crmCtcactActId.crmActTitle`_                          | _char(255)_                              |          |           |          | -                                                                                |

`CrmMeanOfContact` business object definition
---------------------------------------------



### Fields

| Name                                                         | Type                                     | Required | Updatable | Personal | Description                                                                      |
|--------------------------------------------------------------|------------------------------------------|----------|-----------|----------|----------------------------------------------------------------------------------|
| `crmMocPriority`                                             | enum(1) using `CRM_MOC_PRIORITY` list    | yes      | yes       |          | -                                                                                |
| `crmMocType`                                                 | enum(20) using `CRMMOCTYPE` list         | yes      | yes       |          | -                                                                                |
| `crmMocContent`                                              | char(30)                                 | yes*     | yes       |          | -                                                                                |
| `crmMocCtcId` link to **`CrmContact`**                       | id                                       | yes      | yes       |          | -                                                                                |
| _Ref. `crmMocCtcId.crmCtcName`_                              | _char(30)_                               |          |           |          | -                                                                                |
| _Ref. `crmMocCtcId.crmCtcFirstName`_                         | _char(40)_                               |          |           |          | -                                                                                |

### Lists

* `CRM_MOC_PRIORITY`
    - `1` 
    - `2` 
    - `3` 
* `CRMMOCTYPE`
    - `Email` Email
    - `Phone` Mobile
    - `Fax` Fax

`CrmOppPrd` business object definition
--------------------------------------



### Fields

| Name                                                         | Type                                     | Required | Updatable | Personal | Description                                                                      |
|--------------------------------------------------------------|------------------------------------------|----------|-----------|----------|----------------------------------------------------------------------------------|
| `crmOppprdOppId` link to **`CrmOpportunity`**                | id                                       | yes*     | yes       |          | -                                                                                |
| _Ref. `crmOppprdOppId.crmOppTitle`_                          | _char(255)_                              |          |           |          | -                                                                                |
| `crmOppprdPrdId` link to **`CrmProduct`**                    | id                                       | yes*     | yes       |          | -                                                                                |
| _Ref. `crmOppprdPrdId.crmPrdLabel`_                          | _char(30)_                               |          |           |          | -                                                                                |
| _Ref. `crmOppprdPrdId.crmPrdPrice`_                          | _float(11, 2)_                           |          |           |          | -                                                                                |
| `crmOppprdQuantity`                                          | int(11)                                  |          | yes       |          | -                                                                                |
| _Ref. `crmOppprdPrdId.crmPrdBillingMethod`_                  | _enum(255) using `CRMPRDBILLINGMETHOD` list_ |          |           |          | -                                                                                |
| _Ref. `crmOppprdPrdId.crmPrdReference`_                      | _char(255)_                              |          |           |          | -                                                                                |
| _Ref. `crmOppprdPrdId.crmPrdDocuments`_                      | _document_                               |          |           |          | -                                                                                |

### Lists

* `CRMPRDBILLINGMETHOD`
    - `Unitary` UNI
    - `Daily` DAY
    - `Weekly` WEE
    - `Monthly` MON
    - `Yearly` YEA

`CrmOppCtc` business object definition
--------------------------------------



### Fields

| Name                                                         | Type                                     | Required | Updatable | Personal | Description                                                                      |
|--------------------------------------------------------------|------------------------------------------|----------|-----------|----------|----------------------------------------------------------------------------------|
| `crmOppctcOppId` link to **`CrmOpportunity`**                | id                                       | yes*     | yes       |          | -                                                                                |
| _Ref. `crmOppctcOppId.crmOppTitle`_                          | _char(255)_                              |          |           |          | -                                                                                |
| `crmOppctcCtcId` link to **`CrmContact`**                    | id                                       | yes*     | yes       |          | -                                                                                |
| _Ref. `crmOppctcCtcId.crmCtcName`_                           | _char(30)_                               |          |           |          | -                                                                                |
| _Ref. `crmOppctcCtcId.crmCtcFirstName`_                      | _char(40)_                               |          |           |          | -                                                                                |

`CrmCompOpp` business object definition
---------------------------------------



### Fields

| Name                                                         | Type                                     | Required | Updatable | Personal | Description                                                                      |
|--------------------------------------------------------------|------------------------------------------|----------|-----------|----------|----------------------------------------------------------------------------------|
| `crmCompoppCompId` link to **`CrmCompetitor`**               | id                                       | yes*     | yes       |          | -                                                                                |
| _Ref. `crmCompoppCompId.crmCompName`_                        | _char(50)_                               |          |           |          | -                                                                                |
| _Ref. `crmCompoppCompId.crmCompComment`_                     | _text(1000)_                             |          |           |          | -                                                                                |
| `crmCompoppOppId` link to **`CrmOpportunity`**               | id                                       | yes*     | yes       |          | -                                                                                |
| _Ref. `crmCompoppOppId.crmOppTitle`_                         | _char(255)_                              |          |           |          | -                                                                                |
| `crmCompoppDescription`                                      | text(100)                                |          | yes       |          | -                                                                                |
| _Ref. `crmCompoppOppId.crmOppLeadId`_                        | _id_                                     |          |           |          | -                                                                                |
| _Ref. `crmCompoppOppId.crmOppComment`_                       | _text(2000)_                             |          |           |          | -                                                                                |
| _Ref. `crmCompoppOppId.crmOppAmount`_                        | _float(11, 2)_                           |          |           |          | -                                                                                |

`CrmActCol` business object definition
--------------------------------------



### Fields

| Name                                                         | Type                                     | Required | Updatable | Personal | Description                                                                      |
|--------------------------------------------------------------|------------------------------------------|----------|-----------|----------|----------------------------------------------------------------------------------|
| `crmActcolActId` link to **`CrmActivity`**                   | id                                       | yes*     | yes       |          | -                                                                                |
| _Ref. `crmActcolActId.crmActId`_                             | _int(11)_                                |          |           |          | -                                                                                |
| _Ref. `crmActcolActId.crmActWhen`_                           | _datetime_                               |          |           |          | -                                                                                |
| _Ref. `crmActcolActId.crmActTitle`_                          | _char(255)_                              |          |           |          | -                                                                                |
| _Ref. `crmActcolActId.crmActivityCrmActTypefk`_              | _id_                                     |          |           |          | -                                                                                |
| _Ref. `crmActivityCrmActTypefk.crmActTypeLabel`_             | _char(255)_                              |          |           |          | -                                                                                |
| _Ref. `crmActcolActId.crmActDescription`_                    | _text(2000)_                             |          |           |          | -                                                                                |
| `crmActcolColId` link to **`CrmCollaborator`**               | id                                       | yes*     | yes       |          | -                                                                                |
| _Ref. `crmActcolColId.usr_login`_                            | _regexp(100)_                            |          |           | yes      | _Login_                                                                          |
| _Ref. `crmActcolColId.usr_first_name`_                       | _char(50)_                               |          |           | yes      | _First name_                                                                     |
| _Ref. `crmActcolColId.usr_last_name`_                        | _char(50)_                               |          |           | yes      | _Last name_                                                                      |
| _Ref. `crmActcolColId.usr_email`_                            | _email(100)_                             |          |           | yes      | _Email address_                                                                  |
| _Ref. `crmActcolColId.usr_cell_num`_                         | _phone(20)_                              |          |           | yes      | _Mobile/cellular phone number_                                                   |

