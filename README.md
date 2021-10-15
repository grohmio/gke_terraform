# gke_terraform

## Setup
This steps are mandatory to create a gke cluster in a gcp project.

### Prerequisits
* terraform
* gcp account
* gcp project, [enabled compute engine api](https://console.cloud.google.com/apis/library/compute.googleapis.com), [enabled kubernetes engine api](https://console.cloud.google.com/apis/api/container.googleapis.com/overview)
* [gcp service account](https://cloud.google.com/docs/authentication/production#create_service_account)


## Setup
* after creating service account save your key file `*.json` in folder `.keys`

* add credentials to terrafaorm via environment variable
```
export GOOGLE_APPLICATION_CREDENTIALS=*.json
```
* change `projectid` in file `terraform.tfvars`

### Init
```console
$ terraform init --reconfigure
```

## Deploy

* validate
```console
$ terraform validate
```

* plan
```console
$ terraform plan -out "planfile"
```

* apply
```console
$ terraform apply "planfile"
```

* destroy
```console
$ terraform destroy
```

## Further readings
* [gcp regions and zones](https://cloud.google.com/compute/docs/regions-zones)