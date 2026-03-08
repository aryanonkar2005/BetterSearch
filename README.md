<h1 align="center">BetterSearch</h1>

<p align="center">
An LLM-driven search platform that extends the capabilities and addresses the limitations of conventional search systems being used by most e-commerce and property listing sites.
</p>
<p align="center">
BetterSearch proposes a new architecture that enables search engines to reason, understand intent, interpret visual content, perform site suitability analysis and deliver more relevant results for long and complex queries that require high reasoning, all while maintaining low latency
</p>

<h2>Key Capabilities</h2>

</p>

- **Natural Language & Intent Understanding**
  - It can understand human language and intent. It can provide relevant results for long and complex queries that traditional search engines fail to resolve.
  - It can perform long reasoning, calculations and script execution if necessary to answer the long and complex query.
  - It also has access to up-to-date information from the web that it might use to answer search queries.

- **Spatial Intelligence**
  - Can perform advanced spatial analysis and geoprocessing operations such as buffering, overlay, network analysis, and raster/vector processing.
  - Can conduct site suitability analysis using techniques like weighted overlay and many more to evaluate and rank potential locations based on multiple spatial factors and constraints.
  - It is connected to spatial data related to demographics, crime, satellite imagery, flight routes, business coordinates and details, infrastructure layers (road, train netowrks) etc.
  - It has access to dynamic real-time data streams such as traffic conditions, weather updates, and Air Quality Index (AQI), enabling timely spatial decision-making and situational awareness.

- **Improved Search Architecture**
  - It delivers significantly more relevant results by proposing a better architecture that addresses the limitations of embedding based candidate retrieval, ranking models etc.

- **Visual Feature-Based Product Search**
  - It enables users to search by describing a product’s visual features ensuring relevant results even when sellers haven’t included those details in the product description.
  - It eliminates the need for sellers to describe product images. The seller only needs to provide details about the product that are not visible in the images and cannot be inferred from the web.

- **Performance Optimizations**
  - It introduces multiple optimizations to keep the latency low.  It automatically detects whether a query requires LLMs, ensuring that simple queries that do not require reasoning, world knowledge, web access, or complex geoprocessing operations are handled without using LLMs.
  - It also allows users to choose between a faster mode that avoids LLMs and a more advanced mode that leverages LLMs with spatial analysis to deliver more relevant results, albeit with slightly higher latency.

</p>

<h2>Limitations of Conventional Search Engines</h2>

<p>
Conventional search engines that rely on ANN algorithms and models such as CLIP for candidate retrieval often produce irrelevant results because they assume that high embedding similarity directly implies high relevance. Two phrases may show a high embedding similarity score simply because they contain synonymous or closely related words. For example, the query “red jacket worn by Michael Jackson in the Thriller music video 1983” may rank“Men's Thriller Style Red Dance Jacket Halloween Costume Replica” highly due to shared terms, even though it isn’t the desired item. The actual desired product—“MJJ Productions Official Retro Leather Outfit MJT-1983 Limited Edition”—might receive a lower similarity score despite being the correct match. To resolve a query like “the t-shirt this celebrity wore at the Met Gala” requires knowledge of the event and the person; ANN search may instead retrieve generic celebrity-style shirts whose descriptions contain words like fashion, event, or celebrity inspired.
</p>

<p>
Image embeddings behave similarly: two objects that look alike may represent completely different products. For instance, a USB flash drive shaped like a key may retrieve actual metal keys, because their shapes are visually similar. Multimodal models such as CLIP align images and text by similarity, but they still lack deeper reasoning. To reach the desired product Embedding Models and Approximate Nearest Neighbour algorithms aren't enough as they don't have reasoning capabilities.
</p>

<h2>Problems with Conventional Search Engines that BetterSearch Addresses</h2>

<p>
The image search feature offered by ecommerce sites can only find products that look visually similar to the provided image. They cannot handle textual search queries that require understanding all the details visible within images of products or properties listed on the platform. Conventional search engines rely heavily on product descriptions. If a t-shirt’s description doesn’t mention the phrase printed on it, a query like “Show me t-shirts with this specific phrase written on them” won’t return that t-shirt in the results. BetterSearch eliminates this need for sellers to describe product images. The seller only needs to provide details about the product that are not visible in the images and cannot be inferred from the web. Users can simply search by describing the product’s visual features.
</p>

<p>
Search engines on property listing sites can typically answer only simple queries like “2 BHK in Hisar” or “Rental properties near the airport.” Resolving these queries does not require complex spatial reasoning or knowledge of demographics, geography, traffic, AQI, etc. Conventional search engines can neither perform geoprocessing operations on spatial data nor conduct site suitability analysis to resolve complex spatial queries like the ones given below.
</p>

<h2>Examples of Queries BetterSearch Can Resolve</h2>

<ol>
<li>Show all apartments inside the area I’ve marked on the attached map. Rank them based on proximity to the red dot marked on the map. All apartments must have a marble island in the kitchen.</li>

<li>List rental properties under ₹20,000 in Hisar that are within 15 minutes of this building (5PCG+MW Hisar, Haryana), within 1 km of a hospital, but away from highways and busy roads. Rank them based on proximity to the building.</li>

<li>मुझे एक dark green टी-शर्ट दिखाओ जिस पर white color की ink से “Wanted” लिखा हो।</li>

<li>Find a 5,000–8,000 sq. ft. commercial property in Haryana suitable for opening a supermarket, where within a 10-minute drive-time isochrone:
 <ol>
 <li>The population density exceeds 10,000 people
 <li>The average household income is above ₹8 LPA
 <li>There are fewer than 2 large supermarkets
</ol>

<p>This image proves that this t-shirt is available on Flipkart.</p>

<p align="center">
<img width="1498" height="916" alt="Screenshot 2026-03-06 164915" src="https://github.com/user-attachments/assets/8e253f52-be5e-47b3-95bb-45736d917816" />
</p>

<p>
Flipkart failed to show the above t-shirt in search results and gave totally irrelevant results because its search system cannot properly understand natural human language. Additionally, sellers rarely describe clothing designs in detail, and Flipkart lacks the capability to interpret product images to match such queries.
 
</p>

<p align="center">
<img width="1900" height="801" alt="Screenshot 2026-03-06 162826" src="https://github.com/user-attachments/assets/5846b6ff-69b8-4060-9d12-2b205a1c5e4c" />
</p>
