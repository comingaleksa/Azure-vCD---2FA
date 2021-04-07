# vCloud SAML autentifikacija sa Azure AD-om

U nastavku je opisan proces konfiguracije AAD-a i vCloud direktora za potrebe 2FA.

__Proces ukratko:__

1. Kreiranje Enterprise App u Azuru
2. Dodavanje korisnika u aplikaciju
3. Podešavanje atributa i claimova aplikacije
4. Podešavanje federation entity za vCD
5. Import vCloud federation metadata to AzureAD
6. Importovanje korisnika u vCD-u
7. Testiranje funkcionalnosti

Pre nego počnemo:

__Morate imati neku od sledećih titula na Azuru:__

``` 
 * Global Administrator
 * Cloud Application Administrator
 * Application Administrator
 * Owner of the service principal.
```

##  __Kreiranje Enterprise aplikacije na Azuru__

 Kao početni korak, ulogovaćemo se na [Azure portal](https://portal.azure.com). </br>

![Login on Azure](azurelogin.png)


 Nakon logovanja, dobijamo mogućnost kreiranja Enterprise aplikacije. </br>
 Ako se Enterprise aplikacija ne pojavi na početnom ekranu, možemo je pretražiti u Search bar-u.</br>
 Kreiramo novu aplikaciju za naše potrebe klikom na dugme New Application, slika ispod.


![Azure create Enterprise app](azureenterpriseapp.png)
