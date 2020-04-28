- Comparing AnimaChaotic Information Extraction system, with ClausIE and AllenNLP semantic role labelling
- To understand SRL labelles extrated by ALLenNLP
  - Arg0:	PROTO-AGENT
  - Arg1: PROTO-PATIENT
  - Arg2:	usually:	benefactive,	instrument,	attribute,	or	end	state
  - Arg3:	usually:	start	point,	benefactive,	instrument,	or	attribute
  - Arg4	the	end	point
  - (Arg2-Arg5	are	not	really	that	consistent,	causes	a	problem	for	labeling)

- CLausIE may extract multiple things from One sentnce, Therefore you might see repitition


- Sentence 1:
  - The elder brother was disappointed with the number of apples.
| Our proposed IE           | ClausIE                                                                 | AllenNLP SRL                                 |
| ------------------------: |:-----------------------------------------------------------------------:|:--------------------------------------------:|
| Subject: The elder brother| Subject: The elder brother                                              |  Verb: was                                   |
| Verb: disappointed        | verb: was                                                               |  ARG1: The elder brother                     |
| Description_Verb: Emotion | indirectobject:                                                         |  ARG2: disappointed with the number of apples|
| Direct Object             | direct object:                                                          |                                              |
| InDirectObject            | complement: disappointed with  the number  apples                       |                                              |
| Time:                     | adverb:                                                                 |                                              |
| Place:                    | Subject: The elder brother                                              |                                              |
| Emotion                   | Verb:was                                                                |                                              |
| Spatail Position:         | IndirectObject:                                                         |                                              |
| Instrument:               | DirectObject:                                                           |                                              |
| Negation: False           | complement: disappointed with the number apples, with the number apples |                                              |
| Speech                    | Adverb:                                                                 |                                              |
| Imperative:               |                                                                         |                                              |

- Sentence 2:
  - The magical tree instead showered upon the elder brother hundreds upon hundreds of tiny needles.
| Our proposed IE                                       | ClausIE                                                                 | AllenNLP SRL                                 |
| ----------------------------------------------------: |:-----------------------------------------------------------------------:|:--------------------------------------------:|
| Subject: a magical tree                               | Subject: The magical tree                                               |  Verb: Showerd                               |
| Verb: shower_on                                       | verb: showered                                                          |  ARG0: The magical tree                      |
| Description_Verb:                                     | indirectobject:                                                         |  ARG1: hundreds upon hundreds of tiny needles|
| Direct Object: hundreds upon hundreds of tiny needles | direct object: hundreds                                                 |  ARG2: upon the elder brother                |
| InDirectObject: The elder brother                     | complement:                                                             |  Adverbial: instead                          |
| Time:                                                 | adverb:  instead                                                        |                                              |
| Place:                                                | Subject: The magical tree                                               |                                              |
| Emotion                                               | Verb: showered                                                          |                                              |
| Spatail Position:                                     | IndirectObject:                                                         |                                              |
| Instrument:                                           | DirectObject: hundreds                                                  |                                              |
| Negation: False                                       | complement: upon the elder brother                                      |                                              |
| Speech                                                | Adverb:                                                                 |                                              |
| Imperative:                                           | Subject: The magical tree                                               |                                              |
|                                                       | Verb: showered                                                          |                                              |
|                                                       | Indirect Object:                                                        |                                              |
|                                                       | Direct Object: hundreds                                                 |                                              |
|                                                       | Complement:                                                             |                                              |
|                                                       | adverb: of tiny needles                                                 |                                              |


- Sentence 3:
  - She asked: "Mum, I need your advice for the concert"
| Our proposed IE                                 | ClausIE                                                                 | AllenNLP SRL                                 |
| ----------------------------------------------: |:-----------------------------------------------------------------------:|:--------------------------------------------:|
| Subject: She                                    | Subject: She                                                            |  Verb: asked                                 |
| Verb: say                                       | verb: asked                                                             |  ARG0: She                                   |
| Description_Verb:                               | indirectobject:                                                         |  ARG1: I need your advice for the concert    |
| Direct Object                                   | direct object: advice                                                   |                                              |
| InDirectObject                                  | complement: Mum, I need your advice for the concert                     |                                              |
| Time:                                           | adverb:                                                                 |                                              |
| Place:                                          |                                                                         |                                              |
| Emotion                                         |                                                                         |                                              |
| Spatail Position:                               |                                                                         |                                              |
| Instrument:                                     |                                                                         |                                              |
| Negation: False                                 |                                                                         |                                              |
| Speech: Mum, I need your advice for the concert |                                                                         |                                              |
|Imperative: False                                |                                                                         |                                              |


- Sentence 4:
  - Once a hungry fox entered a village.
| Our proposed IE                                 | ClausIE                                                                 | AllenNLP SRL                                 |
| ----------------------------------------------: |:-----------------------------------------------------------------------:|:--------------------------------------------:|
| Subject: a hungry fox                           | Subject: a hungry fox                                                   |  Verb: entered                               |
| Verb: enter                                     | verb: entered                                                           |  ARG0: Hungary fox                           |
| Description_Verb:                               | indirectobject:                                                         |  ARG1:Village                                |
| Direct Object: a village                        | direct object: a village                                                |  Temporal: Once                              |
| InDirectObject                                  | complement:                                                             |                                              |
| Time:                                           | adverb: Once                                                            |                                              |
| Place:                                          |                                                                         |                                              |
| Emotion                                         |                                                                         |                                              |
| Spatail Position:                               |                                                                         |                                              |
| Instrument:                                     |                                                                         |                                              |
| Negation: False                                 |                                                                         |                                              |
| Speech:                                         |                                                                         |                                              |
|Imperative:                                      |                                                                         |                                              |




