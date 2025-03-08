# EUChange

For the goals and the approach of the EUChange Initiative, visit www.euchange.eu. This readme will document the deployment manifests found here.

## Overview

### Solution

This set of manifests is the outcome of the EUChange experiment to deploy a MS 365/Exchange/Teams alternative based on open source components on European infrastructure. The functional core of the solution is NextCloud, with the optional apps for Mail, Calendar and Talk. Since NextCloud is not a mail server in itself, Dovecot is also deployed. To be able to receive e-mail, Postfix is deployed. For user management acros the components, OpenLDAP is included. PHPLDAPAdmin is used to manage users in the OpenLDAP instance. Postgres is used as the database to NextCloud and (in the future) OpenLDAP.

### Conventions

The file names of the manifests propose an order of deployment, alhough this is not (in all cases) critical. For every component there may be a manifest for:
00: Secrets; this contains secrets/password for use in other places within the manifests. All secrets are set to "admin" in these examples.
10: ConfigMap; this contains configuration that is used in rhe deployment. It can be in the form of a configuration file or environment variables.
20: Persistent Volume Claim; this contains the persistent storage that will live after pods were deleted/redeployed
30: Deploymentl this contains the actual deployment manifest
40: Service; this contains the services to expose the deployed component
41: Certificate; this contains a certificate managed by cert-manager
42: Ingress ; this contains the configuration for the ingrress controller/reverse proxy

## Postgres


## OpenLDAP

## NextCloud


## PHPLDAPAdmin

## Dovecot

## Postfix

