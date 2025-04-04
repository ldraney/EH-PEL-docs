```mermaid
graph TD;
  A[Order comes in] --> B[SO created by PM, Fulfillment Lead, or Shopify];
  B --> C[PM notifies LM if bulk work is needed with link to SO];
  C --> D[LM prepares work ticket];
  D -->|Includes SO number, batch record, Inflow MO link, complexity points, batch codes, subitems| E{Lab Tech completes work};
  
  E -->|Uploads batch record, Labels three samples: stability, retention, QA| F{ moves ticket to QA};
  F --> G[QA & Tech Lead oversee quality and documentation];
  
  G -->|Lab Tech Lead creates COA| H[QA sample shipped to CTLA];
  G -->|QA uses COA in production| I[Paperwork returned to Tech Lead];
  
  H & I --> J[Lab Tech Lead closes bulk ticket & notifies PM];
  J --> K[PM moves SO forward with production & fulfillment];
  K --> L[PM marks Inflow SO as fulfilled];
  L --> M[Review SO stats and Monday workflow stats in sprints];

```



1. Order comes in and a SO is created by PM, Fulfillment Lead, or Shopify
2. If the SO is created by the PM, PM notifies LM if bulk work is needed.  
3. LM prepares a ticket for work with the following data:
	1. SO number
	2. batch record
	3. Inflow MO link
	4. points for complexity/time
	5. batch code(s) and potential subitems
		1. show Helios example on [Monday](https://earthharbor.monday.com/boards/8448285579/pulses/8552544003) and [Inflow](https://app.inflowinventory.com/manufacturing-orders/2c448bdb-bb24-47c0-84ee-2e3a6a0cbdfb)
		2. Talk about if this is an issue moving forward
4. lab tech completes the work 
	1. uploads or links batch record before moving to QA column 
	2. labels three samples with the batch code -- stability, retention, and QA
5. QA and Tech Lead - overseeing processes, quality, and documentation
	1. Lab Tech Lead creates a COA with QA sample, and then ships to CTLA
	2. QA uses COA during production and returns paperwork to Tech Lead for records
6. Lab Tech Lead closes the bulk ticket and notifies PM
7. PM moves SO forward, coordinating with production line and fulfillment, until finally marking Inflow SO as fulfilled.  
8. Every sprint we review and consider SO stats with Monday workflow stats
