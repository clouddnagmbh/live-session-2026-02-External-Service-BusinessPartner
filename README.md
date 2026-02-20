# 🚀 Step-by-Step Workshop Branches


This repository is structured with individual branches representing each major step of the live session:

**Consuming External Services in SAP CAP – Business Partner API**

Each branch reflects a specific development milestone and shows exactly what was added or changed at that stage.

The `main` branch contains the final, fully working end-to-end solution including:

- External SAP API integration
- Custom CAP service layer
- Secure SAP BTP deployment
- Destination configuration
- SAPUI5/Fiori frontend application

---

## 📚 Branch Overview


* [**01-add-external-service**](../../tree/01-add-external-service)

    * **Focus:** Importing the external SAP S/4HANA OData service (`API_BUSINESS_PARTNER`) using `cds import`
    * EDMX → CDS conversion
    * Preparing the project for external integration



* [**02-add-service-definition**](../../tree/02-add-service-definition)

    * **Focus:** Creating a custom CAP service definition (`srv/service.cds`)
    * Exposing selected entities via projections
    * Introducing a service abstraction layer



* [**03-add-service-handler**](../../tree/03-add-service-handler)

    * **Focus:** Implementing runtime logic in `srv/service.js`
    * Connecting to the external API using `cds.connect.to()`
    * Forwarding OData queries dynamically



* [**04-add-mta-file-for-deployment**](../../tree/04-add-mta-file-for-deployment)

    * **Focus:** Adding `mta.yaml`
    * Preparing the CAP project for SAP BTP deployment
    * Defining modules and required resources



* [**05-create-destination**](../../tree/05-create-destination)

    * **Focus:** Configuring SAP BTP Destination service
    * Secure outbound connectivity to SAP API
    * Adjusting cloud security configuration



* [**06-deploy-to-btp**](../../tree/06-deploy-to-btp)

    * **Focus:** Building MTAR archive and deploying to SAP BTP (Cloud Foundry)
    * Binding required services
    * Verifying cloud runtime



* [**07-add-ui**](../../tree/07-add-ui)

    * **Focus:** Adding SAPUI5 / Fiori frontend
    * Binding UI to deployed OData V4 service
    * Completing full-stack CAP architecture



---

## 🏗 Final Architecture

The completed solution follows this architecture:

Browser  
→ SAPUI5 / Fiori Application  
→ CAP OData Service (SAP BTP)  
→ Destination Service  
→ External SAP S/4HANA Business Partner API  

---

## 🧭 How to Use These Branches

You can explore a specific development step locally by checking out the corresponding branch:

```bash
# Example: Switch to the deployment preparation step
git checkout 04-add-mta-file-for-deployment
```

Each branch builds incrementally on the previous one, allowing you to follow the entire implementation process step by step.

---

## 🎯 Learning Goals

By following the branches in order, you will learn:

- How to import and consume external OData services in SAP CAP
- How to implement service handlers
- How to configure SAP BTP Destinations
- How to deploy CAP applications to Cloud Foundry
- How to build full-stack CAP applications with SAPUI5

---

This repository serves as a structured workshop guide for building secure, cloud-ready CAP applications that consume external enterprise services.
