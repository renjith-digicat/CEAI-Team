# Entity Alignment

Ontology Alignment and Entity Alignment are essential concepts in data integration and management, particularly relevant to areas like the Semantic Web and Artificial Intelligence. This article is designed for individuals looking to understand Entity Alignment, offering guidance and resources for both beginners and those planning to incorporate this knowledge into their projects. No previous experience with these topics is assumed.

The first section provides an introduction to Ontology Alignment and Entity Alignment, using real-world examples to illustrate these concepts. Section 2 explains the common terminologies and glossaries, helping readers familiarise themselves with the language used in this field. Section 3 explores Entity Alignment in the context of Knowledge Graphs and Embedding Techniques, detailing how these technologies interact and their significance in data management. The final section, Section 4, lists important articles, academic papers, and includes links to relevant GitHub repositories. This section is a resource for further reading and practical application in the field of Entity Alignment.

This article aims to provide a clear and straightforward understanding of Entity Alignment, making it accessible to those new to the topic and useful for professionals looking to apply these concepts to their projects.


---

To make these ideas easier to understand, let's look at some real-world examples:


### Example 1 - Interoperability in Healthcare

In healthcare, different hospitals and clinics often use varied systems and terminologies to describe medical conditions, treatments, and procedures. Take the disease Diabetes as an example. Different systems might call it by various names. Some use the scientific term 'Diabetes Mellitus', while others specify 'Type 1 Diabetes' or 'Type 2 Diabetes'. Some might even refer to it by its symptoms, like 'Hyperglycemia'. The situation gets more complicated if hospitals or countries use unique codes for it. Plus, regional and language differences add another layer of complexity. Entity and ontology alignment helps in standardising and integrating this diverse data, enabling better patient care, research, and analysis across different healthcare providers.


### Example 2 - E-Commerce Product Categorization

Online shopping platforms source products from various vendors who may use different terminologies for similar items. Flash Drive, USB Drive, USB Stick, Pen Drive, Thumb Drive, Memory Stick etc refers to the same object. Irrespective of what the vendors are using, the e-commerce platform should be capable of identifying the product. Through ontology alignment, these products can be categorised uniformly, making it easier for customers to find what they're looking for and for the platform to manage its inventory.


### Example 3 - Search Engines and Information Retrieval

Search engines need to understand the relationships and similarities between different terms and concepts to provide accurate search results. For example, when a user searches for the term 'Hyperglycemia', the search engine should be able to comprehend the semantic connection between 'Hyperglycemia' and 'Type 2 Diabetes.' In doing so, it can suggest an article that, while it may not specifically mention 'Hyperglycemia,' is still relevant to the query. Entity and ontology alignment play a crucial role in improving the relevance and precision of search queries.


<!-- --- -->

With these practical examples in mind, let's now explore the formal definitions of Ontology Alignment and Entity Alignment.


### Ontology Alignment (OA)

Ontology Alignment refers to the process of finding correspondences between different ontologies. An ontology, in this context, is a specific way of organising information or data. It includes a set of concepts within a domain, and the relationships between those concepts. In a school-related ontology, concepts might include 'Students', 'Teachers', 'Classes', and 'Subjects'. The relationships could be 'Students attend Classes', 'Teachers teach Subjects', and 'Classes cover specific Subjects'. For instance, the concept of 'Students' might be linked to different 'Classes' like Mathematics or History, and these Classes are taught by respective 'Teachers' who specialise in those Subjects. We can think of it as a unique language or a map that a particular group or system uses to understand and categorise information.


### Entity Alignment (EA) Definition

Entity Alignment, on the other hand, deals with matching entities (like data records, objects, or concepts) across different datasets or ontologies. It’s about finding out which items in different knowledge representations actually refer to the same thing.

To further aid in your understanding, below is a glossary of key terms related to Ontology Alignment and Entity Alignment. This list will help explain some of the specialised language used in the field and in the upcoming literature survey.



* **Ontology**:

    An [ontology](https://en.wikipedia.org/wiki/Ontology_(information_science)) is a formal representation of knowledge as a set of concepts within a domain, and the relationships between those concepts. An ontology provides a framework for modelling a domain. An ontology is generally defined using classes (concepts), relationships (properties), and instances (individuals). The purpose of an ontology is to model a domain of knowledge, enabling semantic interoperability, reasoning, and consistency checking.

* **Schema**:

    A schema is also a framework used to represent knowledge. A schema is a blueprint for organising and representing data within a particular domain. It defines the relationships and constraints between data elements. Schemas are typically used in [database](https://en.wikipedia.org/wiki/Database_schema) systems to define how data is stored, accessed, and managed. Schemas provide a rigid structure than Ontology. On the other hand, Ontologies are semantically richer than Schemas and that is the major reason why ontologies are more popular for semantic interoperability and reasoning.

* **Entity**:

    An entity is a distinct thing or concept, represented within an ontology.

* **Matching**:

    The process of identifying similarities between entities from different ontologies.

* **Classes (Concepts)**:

    Classes are the abstract representations of ideas or categories of objects within a domain.


    E.g;
  ```
  * Person
  * Car
  * Mobile Phone
  ```

* **Relationships (Properties)**:

    Relationships are the types of connections that can exist between classes or instances. In formal logic, the term predicate is generally used to represent the connection, but it is rarely used in the context of Ontologies


    E.g;
  ```
  * Owns (a person owns a car)
  * Has a (a person has a phone)
  * A type of (a car is a type of vehicle)
  ```

* **Instances (Individuals)**:

    Instances are specific occurrences of classes.


    E.g;
  ```
  * Rolls-Royce Phantom (an instance of car)
  * iPhone 15 pro (an instance of phone)
  ```

* **Equivalence Relation**:

    An equivalence relation indicates that two entities represent the same concept or object within a particular domain. The equivalence relation is often used to indicate that two classes or individuals are semantically identical, even if they are referred to by different names or labels. Equivalence relation can be applied to classes ("Canine" and "Dog"), properties ("isOwnedBy" and "HasOwner"), or instances ("UK" and "United Kingdom")

* **Equivalence Mapping**:

    A mapping where entities from different ontologies are identified as being the same.

* **Subsumption Mapping**: 

    Identifying superclass-subclass relationships between entities from different ontologies.

* **Correspondence**:

    A relation between two entities, often from different ontologies, identified through the matching process.

* **Mappings**:

    The actual correspondences identified between ontology entities.

* **Alignment**: 

    The set of all mappings found between two or more ontologies.

* **[Entity Alignment](https://en.wikipedia.org/wiki/Knowledge_graph#Entity_alignment)**: 

    Entity alignment typically refers to the process of identifying entities in different data sets or ontologies that are the same or semantically equivalent. It is often used in the context of linking entities across different knowledge bases or ontologies.

* **Entity Matching:**

    Entity matching  involves identifying records that refer to the same entity across different data sources. It focuses more on matching specific instances based on their attributes and property values.

* **[Ontology Alignment](https://en.wikipedia.org/wiki/Ontology_alignment)**:

    The process of finding correspondences between concepts, relationships, and instances from different ontologies. Ontology alignment is a broader term.

* **Knowledge Graph**:

    A [Knowledge Graph(KG)](https://en.wikipedia.org/wiki/Knowledge_graph), as the name suggests, is a graph-structured knowledge base. It represents information as entities (nodes) and relationships (edges) between them. It can represent real world objects, events, or even abstract concepts and their interrelations in the form of a graph data structure. The main purpose of a KG is to store and retrieve factual information, for applications like search engines and question answering systems.



<!-- --- -->

With a quick introduction to the basics of EA, we now turn our focus to its practical applications, particularly in the realm of Knowledge Graphs. This section delves into the detailed ways in which embedding techniques are employed to enhance the efficacy of EA, demonstrating their critical role in aligning and interpreting complex data structures within Knowledge Graphs.


## Entity Alignment with Knowledge Graphs and Embedding Techniques


### Bridging Knowledge Graphs through Embedding Techniques

As we know, Entity Alignment or Entity Matching identifies entities across data sources that refer to the same entity. Knowledge Graph(KG) based embedding methods have recently dominated EA techniques. Such EA methods map entities to a low-dimension space and align them based on their similarities.

The rise of the internet and multimedia has generated an exponential amount of data. To interpret and use this data efficiently, it needs to be stored in a structured manner. Knowledge Graphs are one such mechanism to store data, leading to its widespread usage. Due to asynchronous data sources, an entity often appears with different aliases in different KGs. This has led to the rise of EA task, which aims to align entities from different KGs referring to the same real world entity.


### Mathematical Formulation

A KG is denoted by **_KG = (T, A, V, E, R)_**, where **T** represents the union of relation and attribute triples, **A** represents the set of attributes, and **E** represents that of entities. All attribute values and relations form the set **V** and **R**, respectively.

Given two KGs, KG1 and KG2, EA aims to identify pairs (e1, e2) where e1 ∈ E1 and e2 ∈ E2 such that e1 and e2 denote the same entity. Some methods make use of a pre-aligned set of entity pairs as training labels which generally is referred to as seeds.


### Evaluation Metrics for EA

The following metrics are generally used for evaluating knowledge graph embedding and entity alignment tasks.



* **Mean Rank:** the average of the _ranks_ of all _positives_  (lower is better, best is 1). 
    * In this instance **rank** refers to the rank assigned by the model to the correct/positive entities in the list of candidate entities output by a model.
* **Mean Reciprocal Rank (MRR):** the average of the reciprocal of the ranks of all positives (higher is better, best is 1).
* **Hits@1:** the fraction of positives that rank better than all their negatives, i.e., have a rank of 1 (higher is better, best is 1).
* **Hits@10:** the fraction of positives that rank in the top 10 among their negatives (higher is better, best is 1).


<!-- --- -->


## Categorising EA approaches

In this section, we briefly look at the different ways EA may be categorised. This is very useful for:



* Deciding if EA is right for you: If you're wondering whether EA is what you need for your project or problem, this section will help you figure that out.
* Using EA in your solution: You'll get ideas on how you can use EA for what you're working on.
* Choosing the right EA approach: There are many ways to do EA, and this section will help you understand which method might work best for your specific needs.

The different ways of categorisation are:



* **Based on Use of Embedding:** Most prominent EA methods involve generating an embedding of entities that need to be compared. The approaches differ in what information they use to create the embedding (structure of the knowledge graph, relations, attributes, and values) and the way they create embeddings (using Transformer based architectures, language based embedding models, multi-modal embeddings, graph convolutional neural networks, or similar methods).
* **Based on structure, relation and attribute awareness.** Based on the information they utilise to align the entities, we could classify EA methods in to the following categories 
    * Structure aware
    * Structure and Relation aware
    * Structure and Attribute aware
* **Based on information used to model the representation.** Another way to classify the EA methods is to consider the information used. Information used could be Relations, Attributes, Textual, and Multimodal (text + images).
* **Based on the learning strategy.** We should also consider the learning strategy used considering the amount of labelled data available to classify the EA approaches. It could be supervised, self-supervised, or unsupervised.


---


## Related Papers and code

In the evolving field of entity alignment, numerous studies have significantly contributed to our understanding and application of this technology. The following list presents a curated selection of noteworthy publications in this domain. Each entry not only provides a direct link to the respective publication but, where available, also includes access to the corresponding codebases. This integration of literature and practical resources aims to offer a comprehensive overview for researchers and practitioners, facilitating deeper engagement with the key developments and methodologies that have shaped the current landscape of entity alignment.


<table>
  <tr>
   <td><strong></strong>
   </td>
   <td><strong>Title</strong>
   </td>
   <td><strong>Summary</strong>
   </td>
   <td><strong>Links</strong>
   </td>
  </tr>
  <tr>
   <td>
<h4>1</h4>


   </td>
   <td>
<h4>A comprehensive survey of entity alignment for knowledge graphs</h4>


   </td>
   <td>This paper investigated almost all the latest knowledge graph “representations learning” and entity alignment methods and summarised their core technologies and features from different aspects. Their full investigation gives a comprehensive outlook on several promising research directions for future work. They also provide an efficient entity alignment toolkit to help researchers quickly start their own entity alignment models.
   </td>
   <td><a href="https://www.sciencedirect.com/science/article/pii/S2666651021000036">A comprehensive survey of entity alignment for knowledge graphs - ScienceDirect</a>
<p>
EAkit—Entity alignment toolkit:
<p>
<a href="https://github.com/THU-KEG/EAkit">GitHub - THU-KEG/EAkit: Entity Alignment toolkit (EAkit), a lightweight, easy-to-use and highly extensible PyTorch implementation of many entity alignment algorithms.</a>
<p>
<a href="https://github.com/nju-websoft/OpenEA">GitHub - nju-websoft/OpenEA: A Benchmarking Study of Embedding-based Entity Alignment for Knowledge Graphs, VLDB 2020</a>
   </td>
  </tr>
  <tr>
   <td>
<h4>2</h4>


   </td>
   <td>
<h4>Entity Alignment For Knowledge Graphs: Progress, Challenges, and Empirical Studies</h4>


   </td>
   <td>This paper presents a comprehensive analysis of various existing EA methods, elaborating their applications and limitations. Further, it distinguishes the methods based on their underlying algorithms and the information they incorporate to learn entity representations. 
<p>
Based on challenges in industrial datasets, this paper brings forward 4 research questions <strong>(RQs)</strong>. These RQs empirically analyse the algorithms from the perspective of 1)Hubness 2)Degree distribution 3)Non-isomorphic neighbourhood, and 4)Name bias. 
<p>
For Hubness, where one entity turns up as the nearest neighbour of many other entities, the paper defines an h-score to quantify its effect on the performance of various algorithms. Additionally, the paper tries to level the playing field for algorithms that rely primarily on name-bias existing in the benchmarking open-source datasets by creating a low name bias dataset. 
<p>
The authors provide an open-source repository for 14 embedding-based EA methods and present the analysis for invoking further research motivations in the field of EA.
   </td>
   <td><a href="https://arxiv.org/abs/2205.08777">[2205.08777] Entity Alignment For Knowledge Graphs: Progress, Challenges, and Empirical Studies</a>
   </td>
  </tr>
  <tr>
   <td>
<h4>3</h4>


   </td>
   <td>
<h4>SelfKG: Self-Supervised Entity Alignment in Knowledge Graphs</h4>


   </td>
   <td>Self-supervised learning is a type of machine learning that does not require labelled data. Instead, it learns from unlabeled data by creating pretext tasks.
<p>
In this paper, the authors propose a self-supervised learning approach to entity alignment called SelfKG. SelfKG learns to distinguish between positive and negative entity pairs by pushing the positive pairs closer together and the negative pairs further apart.
<p>
The authors evaluated SelfKG on two benchmark datasets and showed that it can achieve comparable results to state-of-the-art supervised methods without any labelled data.
   </td>
   <td><a href="https://arxiv.org/pdf/2203.01044.pdf">https://arxiv.org/pdf/2203.01044.pdf</a>
<p>
<a href="https://github.com/THUDM/SelfKG">https://github.com/THUDM/SelfKG</a>
   </td>
  </tr>
  <tr>
   <td>
<h4>4</h4>


   </td>
   <td>
<h4>BERT-INT: A BERT-based Interaction Model For Knowledge Graph Alignment</h4>


   </td>
   <td>This work presents an interaction model to only leverage the side information. Instead of aggregating neighbours, it computes the interactions between neighbours which can capture fine-grained matches of neighbours. Similarly, the interactions of attributes are also modelled.
<p>
The authors treat entity alignment as the downstream objective to finetune a pre-trained BERT model.
<p>
Need labelled training data. Can perform well on monolingual data.
<p>
Authors first construct the training data D = {(e, e′+, e′−)}, where each triplet (e, e′+, e′−) ∈ D contains a queried entity e ∈ E, the rightly aligned counterpart e′+ ∈ E′ and a negative counterpart e′− randomly sampled from E′.
   </td>
   <td><a href="https://dl.acm.org/doi/abs/10.5555/3491440.3491879">BERT-INT: a BERT-based interaction model for knowledge graph alignment</a>
<p>
<a href="https://github.com/kosugi11037/bert-int">https://github.com/kosugi11037/bert-int</a>
   </td>
  </tr>
  <tr>
   <td>
<h4>5</h4>


   </td>
   <td>
<h4>MEAformer: Multi-modal Entity Alignment Transformer for Meta Modality Hybrid</h4>


   </td>
   <td>Multi-modal entity alignment (MMEA) aims to discover identical entities across different knowledge graphs (KGs) whose entities are associated with relevant images. However, current MMEA algorithms rely on KG-level modality fusion strategies for multi-modal entity representation, which ignores the variations of modality preferences of different entities, thus compromising robustness against noise in modalities such as blurry images and relations. 
<p>
This paper introduces MEAformer, a multi-modal entity alignment transformer approach for meta modality hybrid, which dynamically predicts the mutual correlation coefficients among modalities for more fine-grained entity-level modality fusion and alignment. Experimental results demonstrate that our model not only achieves SOTA performance in multiple training scenarios, including supervised, unsupervised, iterative, and low-resource settings, but also has a limited number of parameters, efficient runtime, and interpretability.
   </td>
   <td><a href="https://arxiv.org/pdf/2212.14454v4.pdf">https://arxiv.org/pdf/2212.14454v4.pdf</a>
<p>
<a href="https://github.com/zjukg/MEAformer">https://github.com/zjukg/MEAformer</a>
   </td>
  </tr>
  <tr>
   <td>
<h4>6</h4>


   </td>
   <td>
<h4>MultiKE - Multi-view Knowledge Graph Embedding for Entity Alignment</h4>


   </td>
   <td>In this paper, authors propose a novel framework that unifies multiple views of entities to learn embeddings for entity alignment. Specifically, they embed entities based on the views of entity names, relations and attributes, with several combination strategies. 
   </td>
   <td><a href="https://arxiv.org/abs/1906.02390">https://arxiv.org/abs/1906.02390</a>
   </td>
  </tr>
  <tr>
   <td>
<h4>7</h4>


   </td>
   <td>
<h4>UEA - Towards Entity Alignment in the Open World: An Unsupervised Approach</h4>


   </td>
   <td>This paper offers an unsupervised framework that performs EA in the open world. First, they mine useful features from the side information of KGs. Then, they devise an unmatchable entity prediction module to filter out unmatchable entities and produce preliminary alignment results. These preliminary results are regarded as the pseudo-labeled data and forwarded to the progressive learning framework to generate structural representations, which are integrated with the side information to provide a more comprehensive view for alignment. Finally, the progressive learning framework gradually improves the quality of structural embeddings and enhances the alignment performance by enriching the pseudo-labeled data with alignment results from the previous round.
   </td>
   <td><a href="https://arxiv.org/abs/2101.10535">https://arxiv.org/abs/2101.10535</a>
<p>
<a href="https://github.com/DexterZeng/UEA">https://github.com/DexterZeng/UEA</a>
   </td>
  </tr>
  <tr>
   <td>
<h4>8</h4>


   </td>
   <td>
<h4>TransEdge: Translating Relation-contextualized Embeddings for Knowledge Graphs</h4>


   </td>
   <td>This paper proposes a novel edge-centric embedding model TransEdge, which contextualises relation  representations in terms of specific head-tail entity pairs. We refer to such contextualised representations of a relation as edge embeddings and interpret them as translations between entity embeddings. TransEdge achieves promising performance on different prediction tasks. It obtains the state-of-the-art results on embedding-based entity alignment.
<p>
They also show that TransEdge is complementary with conventional entity alignment methods. Moreover, it shows very competitive performance on link prediction as well.
   </td>
   <td><a href="https://arxiv.org/abs/2004.13579">https://arxiv.org/abs/2004.13579</a>
<p>
<a href="https://github.com/nju-websoft/TransEdge">https://github.com/nju-websoft/TransEdge</a>
   </td>
  </tr>
  <tr>
   <td>
<h4>9</h4>


   </td>
   <td>
<h4>KECG - Semi-supervised Entity Alignment via Joint Knowledge Embedding Model and Cross-graph Model</h4>


   </td>
   <td>The basic idea of KECG is to utilise a
cross-graph model to embed entities into a unified
vector space by using inner-graph structure and
inter-graph alignments information; meanwhile
the knowledge embedding model learns KG
representations to implicitly complete different
KGs towards consistency and model relational
constraints among entities. There are two key
points for high-quality joint training. First, the
completion from KG learning may exacerbate
the heterogeneity between two KGs, because two
KGs may contain different rich parts, which shall
become richer during training. Second, different
from conventional KG representation learning,
entity alignment requires one-to-one mapping,
which implies that the similar entities sharing
common neighbours cannot be embedded closely,
otherwise they shall be aligned incorrectly
   </td>
   <td><a href="https://aclanthology.org/D19-1274/">https://aclanthology.org/D19-1274/</a>
<p>
<a href="https://github.com/THU-KEG/KECG">https://github.com/THU-KEG/KECG</a>
   </td>
  </tr>
  <tr>
   <td>
<h4>10</h4>


   </td>
   <td>
<h4>EMGCN - Entity Alignment for Knowledge Graphs with Multi-order Convolutional Networks</h4>


   </td>
   <td>EMGCN guarantees (i) entity consistency – the names of corresponding entities should be equivalent, (ii) relation consistency – the relation is preserved from source KG to target KG, and (iii) attribute consistency – the corresponding entities should have equivalent attributes and equivalent attribute values. 
<p>
They use Relation-aware Multi-order Embedding to achieve this. 
   </td>
   <td><a href="https://ieeexplore.ieee.org/document/9262038">https://ieeexplore.ieee.org/document/9262038</a>
<p>
<a href="https://github.com/vinhsuhi/EMGCN">https://github.com/vinhsuhi/EMGCN</a>
   </td>
  </tr>
  <tr>
   <td>
<h4>11</h4>


   </td>
   <td>
<h4>Cross-lingual knowledge graph alignment via graph matching neural network</h4>


   </td>
   <td>Focused on cross-lingual knowledge graph alignment.
<p>
Aligns neighbourhood subgraphs around entities, using a 2-layer stacked GCN to encode local structural information and a cross-graph attention mechanism for cross-lingual KG representations. 
<p>
Entity embeddings derived only from monolingual KG structural information, which may fail at matching entities that have different facts in two KGs. In this paper, authors introduce the topic entity graph, a local sub-graph of an entity, to represent entities with their contextual information in KG. From this view, the KG-alignment task can be formulated as a graph matching problem; and they further propose a graph-attention based solution, which first matches all entities in two topic entity graphs, and then jointly model the local matching information to derive a graph-level matching vector. 
   </td>
   <td><a href="https://aclanthology.org/P19-1304/">https://aclanthology.org/P19-1304/</a>
   </td>
  </tr>
  <tr>
   <td>
<h4>12</h4>


   </td>
   <td>
<h4>List of state-of-the-art Entity Alignment methods on a list of common datasets</h4>


   </td>
   <td>Evaluation results and links to papers and codes are available here in the <strong>papers with code</strong> website.
   </td>
   <td><a href="https://paperswithcode.com/task/entity-alignment">https://paperswithcode.com/task/entity-alignment</a>
   </td>
  </tr>
</table>

