# Terraform

Terraform outil créer, modifier, versionner les infrastructure. Surcouche pour les providers, il sert à mettre en place rapidement ces derniers.
Terraform peut manager des composant de faible nivau (comme les IaaS) mais aussi composant de haut niveau DNS, SaaS...

Caractéristiques :
- Infra as code
- exec plan
- resource graph
- change automation

Terraform correspond au plus haut nv d'abstraction d'un Data centre.
Peut permettre de configurer plusieurs providers en même temps (ex : AWS et OpenStack)

`terraform plan` -- génére un plan d'action de la configuration. plan inclu toutes les actions faites, montre modif que vas effectuer terraform
`terraform graph` -- permet visualisation du plan 
`terraform apply` -- applique le plan
`terraform show` -- montre les infra en place

- def provider :, ?

## Installation
- dl zip / package exise pour deb ? 
- configuration en Json *.tf.json* ou HCL (hahshiCorp Config Language) extension *.tf*

- lecture fich conf par ordre alphabétique

### Bloc **`provider`**
Configuration du provider (terraform peut contenir plusieurs bloc provider). gère le cycle de vie des ressources (create, read, update, delete)

### Bloc **`resources`**
Resources (composant physique/logiciel) qui existent dans l'infrastructure. 

si on fait une resource "aws_truc", on utilise le provider "aws".

### Variable
fichier .tfvars
`terraform apply -var-file=truc.tfvars`



[link 1](https://www.terraform.io/docs/configuration/variables.html)
[link 2](https://www.terraform.io/docs/providers/)

## Openstack with teraform
config terraform providers (auth) puis config les block (computer /compute ...) dans des resources.
[link 3](https://www.terraform.io/docs/providers/openstack/index.html)


