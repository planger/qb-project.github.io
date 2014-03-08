```scala
// Define your schema 
val issueSchema = obj(
    "id" -> objectId,
    "parentIssue" -> optional(objectId),
    "status" -> enum("pending", "approved", "rejected"),
    "urgence" -> integer(range(1, 5)),
    "comment" -> string(maxLength(2000)),
    "reporter" -> obj(
        "firstName" -> string(length(1, 100)),
        "lastName" -> string(length(1, 100)),
        "email" -> email
    ),
    "creationDate" -> dateTime
)
```
                