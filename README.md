### SPIRE_SPIFFE

#### Helm to deploy SPIRE Server with intermediate CA signed by RootCA

#### For PKI - Follow: 

https://github.com/sedovalx/openssl-scripts 

####  To see the SVID use the below command from SPIRE Server POD.

spiffe://example.org/ns/vkv/sa/nginx --> This is the spiffe id of sample nginx workload pod.

``` k -n spire-server exec -it spire-server-0 -- spire-server x509 mint -output pretty -spiffeID spiffe://example.org/ns/vkv/sa/nginx ```

#### Points:
> CN name can be anything and need not to be a FQDN.
> In this helm values, the names are same as certificate like country, CN etc..