# ch-api-client-typescript

usage:

import { CountriesApi, CountryItemViewModel } from './out/api'; import { Configuration } from './out/configuration';

const models :CountryItemViewModel[] = [];

```
const config = new Configuration({ basePath: 'https://api-int.icloudhospital.com/' })
let result = new CountriesApi(config).apiV1CountriesGet().then(d => console.log(d.data.items.map(t => t.name)))
```

!!! instal openapi-generator 4.3.1 npm install @openapitools/openapi-generator-cli

!!! to change openapi-generator version openapi-generator-cli version-manager list select appropriate version

!!! generate client sdk with following command openapi-generator-cli generate -g typescript-axios -o src -i https://api-int.icloudhospital.com/swagger/v1/swagger.json --type-mappings=DateTime=Date

!!! run build to compile an generate js files npm run build

!!! commit to main branch
