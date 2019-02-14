# Maratona de Conectividade PROADI-SUS digiSUS Infoestrutura HAOC - IHE


-----

### Testes Pré-Connectathon

**Prazo para entrega de resultados: 15/3/2019**

- A lista completa de testes Pré-Connectathon está disponível no sistema Gazelle. Instruções para [acesso aos testes](Technical%20Instructions/tech_inst-6.md).  

> IMPORTANTE: Os testes a seguir estão indicados como "opcionais" no Gazelle mas são obrigatórios para a Maratona de Conectividade no Brasil. A saber:

   - XDS.b Cross-Enterprise Document Sharing  
   
        - ator: Document Source - testes [#5001 (Br_XDS-Src_5001)](Technical%20Instructions/tech_inst-3.md) e [#5002 (Br_XDS-Src_5002)](Technical%20Instructions/tech_inst-3-2.md)  
        - ator: Document Consumer - teste [#5003 (Br_XDS-Cons_5003)](Technical%20Instructions/tech_inst-3-1.md)  

   - PDQv3 Patient Demographics Query

        - ator: Patient Demographics Consumer - testes [#6001 (Br_PM-PDQv3_Cons_6001)](Technical%20Instructions/tech_inst-4.md) e [#6002 (Br_PM_PDQv3_Continuation_6002)](Technical%20Instructions/tech_inst-4-1.md)

   - PIXv3 Patient Identifier Cross-Referencing 

        - ator: Patient Identity Source - teste [#6003 (Br_PM-PIXv3_Src_6003)](Technical%20Instructions/tech_inst-5.md)

-----
### Período de Registro: 7/1/2019 a 20/1/2019


- URL de acesso ao sistema Gazelle: [https://ihe.wustl.edu/gazelle-na/](https://ihe.wustl.edu/gazelle-na/)

- Instruções sobre criação de conta e processo de [Registro de Sistemas](Technical%20Instructions/tech_inst-1.md)

- [Slides](http://www.ihe.org.br/siteWP/connectathon-2019-kickoff/) reunião de Kickoff e [Cronograma](http://www.ihe.org.br/siteWP/connectathon-2019-cronograma/) de atividades

-----

### Perfil IHE XDS.b Cross-Enterprise Document Sharing  


[Considerações sobre o processo de instalação](Technical%20Instructions/tech_inst-2.md) da ferramenta [NIST XDS ToolKit](https://github.com/usnistgov/iheos-toolkit2)

[Projeto SOAPUI](./SOAPUI%20Projects/NIST%20XDS-Toolkit-Examples-soapui-project.xml) com exemplos baseados na utilização da ferramenta NIST XDS ToolKit 

[Schemas & WSDLs](./IHE%20schemas%20&%20wsdls) e [exemplos de mensagens](./IHE%20messages%20examples/XDS.b)

Referências:  

- [IHE ITI Vol 1](https://www.ihe.net/uploadedFiles/Documents/ITI/IHE_ITI_TF_Vol2b.pdf#page=81) - Cross-enterprise Document Sharing
- [IHE ITI Vol 2a ITI-18](https://www.ihe.net/uploadedFiles/Documents/ITI/IHE_ITI_TF_Vol2a.pdf#page=91) - Registry Stored Query
- [IHE ITI Vol 2b ITI-41](https://www.ihe.net/uploadedFiles/Documents/ITI/IHE_ITI_TF_Vol2b.pdf#page=153) - Provide and Register Document Set-b
- [IHE ITI Vol 2b ITI-42](https://www.ihe.net/uploadedFiles/Documents/ITI/IHE_ITI_TF_Vol2b.pdf#page=164) - Register Document Set-b
- [IHE ITI Vol 2b ITI-43](https://www.ihe.net/uploadedFiles/Documents/ITI/IHE_ITI_TF_Vol2b.pdf#page=175) - Retrive Document Set
- [IHE ITI Vol 3](https://www.ihe.net/uploadedFiles/Documents/ITI/IHE_ITI_TF_Vol3.pdf#page=4) - Metadata used in Document Sharing profiles

Forum técnico internacional de [desenvolvedores XDS.b](https://groups.google.com/forum/#!forum/ihe-xds-implementors)

-----

### Perfis IHE Patient Demographics Query (PDQv3) e Patient Identifier Cross-Referencing (PIXv3)

[Projeto SOAPUI](./SOAPUI%20Projects/Gazelle-Patient-Manager-examples-soapui-project.xml) com exemplos de PIXv/PDQv3 baseados na utilização da ferramenta [Gazelle Patient Manager](https://gazelle.ihe.net/PatientManager/home.seam) 

[Projeto SOAPUI](./SOAPUI%20Projects/NIST-PIXPDQ-Examples-soapui-project.xml) com exemplo PDQv3 baseado na utilização da ferramenta [NIST PIX PDQ Tool](https://pixpdqtests.nist.gov/pixpdqtool/) 

[Schemas & WSDLs](./IHE%20schemas%20&%20wsdls) e exemplos de mensagens [PDQv3](./IHE%20messages%20examples/PDQV3) e [PIXv3](./IHE%20messages%20examples/PIXV3) 

Exemplo ilustrativo de mensagem [ITI-44 Patient Identity Feed "Add"](Technical%20Instructions/media/image23.png) com referências para wrappers HL7 v3.

Referências:

- [IHE ITI Vol 1](https://www.ihe.net/uploadedFiles/Documents/ITI/IHE_ITI_TF_Vol1.pdf#page=231) - Patient Identifier Cross-referencing HL&v3
- [IHE ITI Vol 1](https://www.ihe.net/uploadedFiles/Documents/ITI/IHE_ITI_TF_Vol1.pdf#page=236) - Patient Demographics Query HL7v3
- [IHE ITI Vol2b ITI-44](https://www.ihe.net/uploadedFiles/Documents/ITI/IHE_ITI_TF_Vol2b.pdf#page=192) - Patient Identity Feed HL7v3
- [IHE ITI Vol2b ITI-45](https://www.ihe.net/uploadedFiles/Documents/ITI/IHE_ITI_TF_Vol2b.pdf#page=217) - PIXv3 Query
- [IHE ITI Vol2b ITI-47](https://www.ihe.net/uploadedFiles/Documents/ITI/IHE_ITI_TF_Vol2b.pdf#page=245) - Patient Demographics Query HL7v3
- [IHE ITI Vol2x](https://www.ihe.net/uploadedFiles/Documents/ITI/IHE_ITI_TF_Vol2x.pdf#page=59) - HL7 v3 Transmission and Trigger Event Control Act
Wrappers

Forum técnico internacional de desenvolvedores [PIXv3/PDQv3](https://groups.google.com/forum/#!forum/ihe_pix_pdq_testing)

-----
### Perfil Audit Trail and Node Authentication (ATNA)

As mensagens de auditoria são organizadas por transação e respectivos atores sendo utilizados. Por exemplo, a transação ITI-18 "Registry Stored Query" envolve dois atores: "Document Consumer" e "Document Registry". Se o seu sistema irá realizar a Query ele assume o papel do ator "Document Consumer". Após realizar a consulta é necessário enviar uma mensagem de auditoria para o Audit Record Repository (ARR). Na lista de transação/ator abaixo, você encontrará o modelo de informação de mensagem de auditoria para a transação ITI-18 e o ator "Document Consumer".

Um exemplo de todas as mensagens de auditoria listadas a seguir pode ser encontrado neste projeto SOAPUI.

Modelos de informação de mensagens de auditoria por Transação/Ator:

- Transãção XDS.b ITI-41 "Provide and Register Document Set-b"
    
  - Document Source audit Message. Referência: [IHE  ITI vol 2b Section 3.41.5.1.1](https://www.ihe.net/uploadedFiles/Documents/ITI/IHE_ITI_TF_Vol2b.pdf#page=160) 
  - Document Repository audit message. Referência: [IHE ITI vol 2b Section 3.41.5.1.2](https://www.ihe.net/uploadedFiles/Documents/ITI/IHE_ITI_TF_Vol2b.pdf#page=162) 
   
- Transação XDS.b ITI-42 "Register Document Set-b"

  - Document Repository audit message. Referência: [IHE ITI vol 2b Section 3.42.5.1.1](https://www.ihe.net/uploadedFiles/Documents/ITI/IHE_ITI_TF_Vol2b.pdf#page=172)
  - Document Registry audit message. Referência: [IHE ITI vol 2b Section 3.42.5.1.2](https://www.ihe.net/uploadedFiles/Documents/ITI/IHE_ITI_TF_Vol2b.pdf#page=173)

- Transãção XDS.b ITI-43 "Retrieve Document Set"

  - Document Consumer audit message. Referência: [IHE  ITI vol 2b Section 3.43.6.1.1](https://www.ihe.net/uploadedFiles/Documents/ITI/IHE_ITI_TF_Vol2b.pdf#page=189) 
  - Document Repository audit message. Referência: [IHE ITI vol 2b Section 3.43.6.1.2](https://www.ihe.net/uploadedFiles/Documents/ITI/IHE_ITI_TF_Vol2b.pdf#page=190) 

- Transãção XDS.b ITI-18 "Registry Stored Query"

  - Document Consumer audit message. Referência: [IHE ITI vol2a Section 3.18.5.1.1](https://www.ihe.net/uploadedFiles/Documents/ITI/IHE_ITI_TF_Vol2a.pdf#page=128)
  - Document Registry audit message. Referência: [IHE ITI vol2a Section 3.18.5.1.2](https://www.ihe.net/uploadedFiles/Documents/ITI/IHE_ITI_TF_Vol2a.pdf#page=130)

- Transação PIXv3 ITI-44 "Patient Identity Feed HL7 V3"

  - Patient Identity Source audit message. Referência: [IHE ITI vol 2b Section 3.44.5.1.1](https://www.ihe.net/uploadedFiles/Documents/ITI/IHE_ITI_TF_Vol2b.pdf#page=214) 
  -  Patient Identifier Cross-reference Manager audit message. Referência: [IHE ITI vol 2b Section 3.44.5.1.2](https://www.ihe.net/uploadedFiles/Documents/ITI/IHE_ITI_TF_Vol2b.pdf#page=215)
 
- Transação PIXv3 ITI-45 "PIXV3 Query"

  - Patient Identifier Cross-reference Consumer audit message. Referência: [IHE ITI vol 2b Section 3.45.5.1.1](https://www.ihe.net/uploadedFiles/Documents/ITI/IHE_ITI_TF_Vol2b.pdf#page=231) 
  -  Patient Identifier Cross-reference Manager audit message. Referência: [IHE ITI vol 2b Section 3.45.5.1.2](https://www.ihe.net/uploadedFiles/Documents/ITI/IHE_ITI_TF_Vol2b.pdf#page=233)

- Transação PDQv3 ITI-47 "Patient Demographics Query" HL7 V3

  - Patient Demographics Consumer audit message. Referência: [IHE ITI vol 2b Section 3.45.5.1.1](https://www.ihe.net/uploadedFiles/Documents/ITI/IHE_ITI_TF_Vol2b.pdf#page=268) 
  -   Patient Demographics Supplier audit message. Referência: [IHE ITI vol 2b Section 3.45.5.1.2](https://www.ihe.net/uploadedFiles/Documents/ITI/IHE_ITI_TF_Vol2b.pdf#page=270)
 

Referências:

- [IHE ITI Vol 1](https://www.ihe.net/uploadedFiles/Documents/ITI/IHE_ITI_TF_Vol1.pdf#page=68) - Audit Trail and Node Authentication (ATNA) Profile
- [IHE ITI Vol2a ITI-19](https://www.ihe.net/uploadedFiles/Documents/ITI/IHE_ITI_TF_Vol2a.pdf#page=121) - Authenticate Node
- [IHE ITI Vol2a ITI-20](https://www.ihe.net/uploadedFiles/Documents/ITI/IHE_ITI_TF_Vol2a.pdf#page=138) - Record Audit Event

-----

### HL7

- [HL7 v3 edition 2008](./HL7v3%20Edition2008%20cd)

-----

### Outros recursos

Recursos | URL
---------|-----
IHE Internacional | https://www.ihe.net 
IHE Brasil | http://www.ihe.org.br/ 
IHE Technical Frameworks | http://ihe.net/Technical_Frameworks 
Webinar: IHE ITI Framework Introduction | https://youtu.be/609bBW9RmCg 
Webinar: Document Sharing overview | https://www.youtube.com/watch?v=VG1oF5FEijY  
Webinar: Introduction of IHE XDS/Document Sharing | https://youtu.be/zLS1mPxdbMI
NIST XDS ToolKit | https://github.com/usnistgov/iheos-toolkit2
Webinar: Introduction of IHE PIX/PDQv3 Profiles | https://youtu.be/tO6Fd6oJ_3E 
Gazelle Patient Manager | https://gazelle.ihe.net/PatientManager/home.seam
OpenEHR | http://www.openehr.org 
Modelo de informação sumário de alta internação e registro de atendimento clínico | http://www.conass.org.br/conass-informa-n-69-republicada-resolucao-cit-n-33-que-institui-os-modelos-de-informacao-do-sumario-de-alta-e-do-registro-de-atendimento-clinico/ 



