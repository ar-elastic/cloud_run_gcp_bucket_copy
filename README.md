# cloud_run_gcp_bucket_copy

Leverage GCP Event Arc Trigger and CloudRun Function to copy Bucket data

1. Create Service Account with permissions to your GCP source bucket, EventArc and CloudRun. 
2  Use an EvertArc trigger (snapshot added / finalized) to trigger the CloudRun Function
3  Transfer source bucket data to Destination Bucket

**Key Architectural Considerations:**
**Event-Driven: **The architecture is event-driven, meaning it reacts in real-time to changes in the Cloud Storage bucket.
**Scalability: **Cloud Run and Cloud Storage are highly scalable services, so this architecture can handle a large number of events and large files.
**Loose Coupling: **The event-driven nature of the solution creates loose coupling between the source bucket and the data replication process. Changes to the bucket automatically trigger the function without requiring any manual intervention.
