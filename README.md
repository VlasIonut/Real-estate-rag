Salut, mă numesc **Vlas Ionuț** și lucrez la portofoliul de proiecte personale, proiectul ăsta rezolvă o problemă personală cu care se confruntă toată lumea la un moment dat: cautarea unei locuințe, fie prin chirie sau prin cumpărare, iar ținta lui îi de a crea un portofoliu extins ce se actualizează cu anunțuri disponibile gratuit pe internet, cu ajutorul inteligenței artificiale. Este strict pentru uz personal, orice altă utilizare mi-ar aduce urmări legale.
Dacă îți place această idee te invit să explorezi proiectul.

# Real-estate-rag
AI scraper for real estate
### Problema
Analizarea a sute/mii de anunțuri cu un LLM direct = cost enorm de tokeni (fiecare anunț trimis complet la API).

### Soluția RAG (Retrieval-Augmented Generation)
1. Scraping → toate anunțurile devin **embeddings vectoriali** în LanceDB local.
2. La interogare → utilizatorul pune o întrebare (ex: „apartament 2 camere sub 500€, liniștit").
3. **Similarity search** extrage doar top 5-10 anunțuri relevante din sute.
4. Doar acele 5-10 anunțuri sunt trimise la LLM pentru analiză.
5. **Rezultat:** reducere masivă a costurilor de tokeni vs. trimiterea întregului set.

Prin acești pași voi reduce consumul de tokeni necesari pentru a realiza atât proiectul în sine cât și scanarea anunțurilor.
