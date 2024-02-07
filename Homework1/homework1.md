<h1>Module 1 Homework</h1>

<h2>Docker & SQL
In this homework we'll prepare the environment and practice with Docker and SQL</h2>

<h3>Question 1. Knowing docker tags</h3>

Run the command to get information on Docker

<code>docker --help</code>

Now run the command to get help on the "docker build" command:

<code>docker build --help</code>

Do the same for "docker run".

Which tag has the following text? - Automatically remove the container when it exits

- <code>--rm</code>

![image](https://github.com/Oscari012/Oscar-zoomcamp2024/assets/68555999/7e959f36-6b34-4860-839c-15f122242f0f)


<h3>Question 2. Knowing docker tags</h3>

Run docker with the python:3.9 image in an interactive mode and the entrypoint of bash.
Now check the python modules that are installed ( use ```pip list``` ). 

What is version of the package *wheel* ?

- 0.42.0

![image](https://github.com/Oscari012/Oscar-zoomcamp2024/assets/68555999/1b3ab401-82f0-4113-9623-baa2cfe004b6)


<h3>Question 3. Count records</h3>

How many taxi trips were totally made on September 18th 2019?

Tip: started and finished on 2019-09-18. 

Remember that `lpep_pickup_datetime` and `lpep_dropoff_datetime` columns are in the format timestamp (date and hour+min+sec) and not in date.

- 15612

![image](https://github.com/Oscari012/Oscar-zoomcamp2024/assets/68555999/1b85ccff-23e7-4711-b10c-d3043378d59a)


<h3>Question 4. Longest trip for each day</h3>

Which was the pick up day with the longest trip distance? Use the pick up time for your calculations.

- 2019-09-26

![image](https://github.com/Oscari012/Oscar-zoomcamp2024/assets/68555999/b937b051-3072-4aa9-b87b-06ae3be9987d)


<h3>Question 5. Three biggest pick up Boroughs</h3>

Consider lpep_pickup_datetime in '2019-09-18' and ignoring Borough has Unknown

Which were the 3 pick up Boroughs that had a sum of total_amount superior to 50000?

- "Brooklyn" "Manhattan" "Queens"

![image](https://github.com/Oscari012/Oscar-zoomcamp2024/assets/68555999/605b3185-fabb-43a4-86a4-b7e8ceae779e)


<h3>Question 6. Largest tip</h3>

For the passengers picked up in September 2019 in the zone name Astoria which was the drop off zone that had the largest tip? We want the name of the zone, not the id.

- JFK Airport

![image](https://github.com/Oscari012/Oscar-zoomcamp2024/assets/68555999/d0b46115-7b76-4be8-b256-be410aa5a04d)


<h3>Question 7. Creating Resources</h3>

After updating the main.tf and variable.tf files run:

```
terraform apply
```

Paste the output of this command into the homework submission form.

```
Terraform used the selected providers to generate the following execution plan. Resource actions are indicated with the following symbols:
  + create

Terraform will perform the following actions:

  # google_bigquery_dataset.demo_dataset will be created
  + resource "google_bigquery_dataset" "demo_dataset" {
      + creation_time              = (known after apply)
      + dataset_id                 = "demo_dataset"
      + default_collation          = (known after apply)
      + delete_contents_on_destroy = false
      + effective_labels           = (known after apply)
      + etag                       = (known after apply)
      + id                         = (known after apply)
      + is_case_insensitive        = (known after apply)
      + last_modified_time         = (known after apply)
      + location                   = "US"
      + max_time_travel_hours      = (known after apply)
      + project                    = "terraform-413201"
      + self_link                  = (known after apply)
      + storage_billing_model      = (known after apply)
      + terraform_labels           = (known after apply)
    }

  # google_storage_bucket.demo-bucket will be created
  + resource "google_storage_bucket" "demo-bucket" {
      + effective_labels            = (known after apply)
      + force_destroy               = true
      + id                          = (known after apply)
      + location                    = "US"
      + name                        = "terraform-413201-terra-bucket"
      + project                     = (known after apply)
      + public_access_prevention    = (known after apply)
      + self_link                   = (known after apply)
      + storage_class               = "STANDARD"
      + terraform_labels            = (known after apply)
      + uniform_bucket_level_access = (known after apply)
      + url                         = (known after apply)

      + lifecycle_rule {
          + action {
              + type = "AbortIncompleteMultipartUpload"
            }
          + condition {
              + age                   = 1
              + matches_prefix        = []
              + matches_storage_class = []
              + matches_suffix        = []
              + with_state            = (known after apply)
            }
        }
    }

Plan: 2 to add, 0 to change, 0 to destroy.

Do you want to perform these actions?
  Terraform will perform the actions described above.
  Only 'yes' will be accepted to approve.

  Enter a value: yes

google_bigquery_dataset.demo_dataset: Creating...
google_storage_bucket.demo-bucket: Creating...
google_bigquery_dataset.demo_dataset: Creation complete after 1s [id=projects/terraform-413201/datasets/demo_dataset]
google_storage_bucket.demo-bucket: Creation complete after 1s [id=terraform-413201-terra-bucket]
```

