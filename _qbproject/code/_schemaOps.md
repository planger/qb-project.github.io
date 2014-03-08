```scala
// Combine Schemas
val urgentIssueSchema = issueSchema + obj(
    "urgency" -> enum("super important", "meh")
)

// Transform Schemas, e.g. make fields optional
val noReporterSchema = urgendIssueSchema ? "reporter"

```