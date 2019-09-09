# sykmelding-alerts

Lager alerts for team sykmelding sine apper

For mer informasjon om hvordan alarmene fungere se:
`https://github.com/nais/doc/tree/master/content/alerts`

### For NAV ansatte
Vi er tilgjenngelig på slack kanalen #team-sykemdling

## Utvikling:
En kan bruke `https://prometheus.nais.preprod.local/graph` som hjelp til å teste queries. 
Bruk `test/sykemelding_test.yaml` til å teste alerteren i dev. 
Varsel dukker da opp i `sykemelding-alerts-dev` på Slack

### Deploy test:
Deploy alerten din til riktig cluster i preprod:
`kubectl apply -f test/sykemelding_test.yaml`

Om alerten allerede finnes må den fjernes først:
`kubectl delete alert sykemeldingalerts-test`

### Deploy prod:
