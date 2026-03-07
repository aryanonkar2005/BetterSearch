# BetterSearch

An LLM-driven search platform designed to extend the capabilities and address the limitations of conventional search systems being used by most e-commerce and property listing sites, without significantly increasing query latency. It also delivers much more relevant results.

Since it uses LLMs behind the scenes it can understand human language and intent, and has access to up-to-date information from the web that it might use to answer search queries. It can perform GIS operations and ArcGIS-style site suitability analysis to resolve complex spatial queries. It delivers significantly more relevant results by proposing a better architecture that addresses the limitations of embedding models, ANN search, ranking algorithms etc. It can also answer queries that require visual interpretation of images, enabling search even when the seller has not provided a textual description of the product or image. It introduces multiple clever optimizations to keep the latency low.

Simple queries that do not require reasoning, world knowledge, web access, or complex GIS operations won’t use LLMs.

Conventional search engines that rely on ANN algorithms and models such as CLIP for candidate retrieval often produce irrelevant results because they assume that high embedding similarity directly implies high relevance. Two phrases may show a high embedding similarity score simply because they contain synonymous or closely related words. For example, the query “red jacket worn by Michael Jackson in the Thriller music video 1983” may rank“Men's Thriller Style Red Dance Jacket Halloween Costume Replica” highly due to shared terms, even though it isn’t the desired item. The actual desired product—“MJJ Productions Official Retro Leather Outfit MJT-1983 Limited Edition”—might receive a lower similarity score despite being the correct match. A query like “the t-shirt this celebrity wore at the Met Gala” requires knowledge of the event and the person; a model may instead retrieve generic celebrity-style shirts whose descriptions contain words like fashion, event, or celebrity inspired.

Image embeddings behave similarly: two objects that look alike may represent completely different products.
For instance, a USB flash drive shaped like a key may retrieve actual metal keys, because their shapes are visually similar.
Multimodal models such as CLIP align images and text by similarity, but they still lack deeper reasoning.
To reach the desired product Embedding Models and Approximate Nearest Neighbour algorithms aren't enough as they don't have reasoning capabilities.

Problems with conventional search engines that BetterSearch addresses:

The image search feature offered by ecommerce sites can only find products that look visually similar to the provided image. They cannot handle textual search queries that require understanding all the details visible within images of products or properties listed on the platform. Conventional search engines rely heavily on product descriptions. If a t-shirt’s description doesn’t mention the phrase printed on it, a query like “Show me t-shirts with this specific phrase written on them” won’t return that t-shirt in the results. BetterSearch eliminates the need for sellers to describe product images. The seller only needs to provide details about the product that are not visible in the images and cannot be inferred from the web. Users can simply search by describing the product’s visual features.

Search engines on property listing sites can typically answer only simple queries like “2 BHK in Hisar” or “Rental properties near the airport.” Resolving these queries does not require complex spatial reasoning or knowledge of demographics, geography, traffic, AQI, etc. Conventional search engines can neither perform GIS operations on spatial data nor conduct ArcGIS-style site suitability analysis to resolve complex spatial queries like the ones given below.

Examples of queries BetterSearch can resolve:
1. Show all apartments inside the area I’ve marked on the attached map. Rank them based on proximity to the red dot marked on the map. All apartments must have a marble island in the kitchen.
2. List rental properties under ₹20,000 in Hisar that are within 15 minutes of this building (5PCG+MW Hisar, Haryana), within 1 km of a hospital, but away from highways and busy roads. Rank them based on proximity to the building.
3. मुझे एक dark green टी-शर्ट दिखाओ जिस पर white color की ink से “Wanted” लिखा हो।
4. Find a 5000 sq. ft. area anywhere in Haryana (but listed on this property listing site) for building a hospital where, within a 30-minute isochrone, the population of citizens earning ₹12 LPA and above is high and competition is low.
<img width="1498" height="916" alt="Screenshot 2026-03-06 164915" src="https://github.com/user-attachments/assets/8e253f52-be5e-47b3-95bb-45736d917816" />
This image proves that this t-shirt is available on Flipkart.
<img width="1900" height="801" alt="Screenshot 2026-03-06 162826" src="https://github.com/user-attachments/assets/5846b6ff-69b8-4060-9d12-2b205a1c5e4c" />
The search results should include the above t-shirt. However, since Flipkart’s search engine cannot understand human language the way LLMs can, and it also lacks the ability to interpret the visual content of product images, it fails to display relevant results.
