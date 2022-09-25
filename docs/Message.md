

# Message


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **UUID** |  |  [optional] |
|**createdAt** | **OffsetDateTime** |  |  [optional] |
|**status** | [**StatusEnum**](#StatusEnum) |  |  [optional] |
|**reason** | **String** |  |  [optional] |
|**cost** | [**Cost**](Cost.md) |  |  [optional] |
|**inbox** | [**InboxEnum**](#InboxEnum) |  |  [optional] |



## Enum: StatusEnum

| Name | Value |
|---- | -----|
| PENDING | &quot;PENDING&quot; |
| REJECTED | &quot;REJECTED&quot; |



## Enum: InboxEnum

| Name | Value |
|---- | -----|
| INCOMING | &quot;incoming&quot; |
| OUTGOING | &quot;outgoing&quot; |


## Implemented Interfaces

* Serializable


