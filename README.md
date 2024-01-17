# Docking Molecular
#### sumário
# Sites
* Uniprot
```python
https://www.uniprot.org/
```
* Alphafold2
```python
https://colab.research.google.com/github/sokrypton/ColabFold/blob/v1.2.0/AlphaFold2.ipynb
```
* Pubchem
```python
https://pubchem.ncbi.nlm.nih.gov/
```
* Pymol
```python
https://pymol.org/2/
```
* MGLTools
```python
https://ccsb.scripps.edu/mgltools/downloads/
```
* PDB(protein data bank)
```python
https://www.rcsb.org/
```
* Openbabel
```python
https://www.cheminfo.org/Chemistry/Cheminformatics/FormatConverter/index.html
```
* Avogadrp
```python
https://avogadro.cc/
```
# Preparo da proteína
Nessa etapa é explicado como preparar a proteína antes de entrar no seu preparo no app do MGLTools onde tanto faz se for extraída do **uniprot** ou do **PDB** assim esse preparo será abordado mais adiante quando tiver molécula e proteína em mãos 
## Proteína extraida do PDB
****1**.** Verifica a existência da estrutura cristalografada por raio-X no banco de dados do PDB para importar uma estrutura com maior confiabilidade, procurando pelo nome da proteína ou o seu gene promotor
   1.1. Caso encontre baixe a estrutura no formato PDB
   ![image](https://github.com/Tutugb/Docking/assets/125391314/157f7b7f-921b-4ce1-9908-6fb09061f193)
****2**.** Abra proteína no pymol

**2.1.** Retire as águas
   
![image](https://github.com/Tutugb/Docking/assets/125391314/3694eb9e-b237-4190-a4d7-4f8e25a35d37)

   **2.2.** Adicione os hidrogênios polares

    ![image](https://github.com/Tutugb/Docking/assets/125391314/a30cf557-d677-4b9a-98db-90620cbd1b26)

   **2.3.** Exporta a molécula como formato PDB

   ![image](https://github.com/Tutugb/Docking/assets/125391314/dd0585db-f25a-4f8c-be86-965cc83e3499)
## Proteína extraida do Uniprot
**1.**  Verifica a existência da estrutura por homologia no banco de dados do Uniprot para importar uma estrutura com confiabilidade relativa, procurando pelo nome da proteína ou o seu gene promotor.


**1.1.** Caso encontre baixe no formato disponível

![image](https://github.com/Tutugb/Docking/assets/125391314/a72ab6c7-0ef7-4081-ba4e-6956900fa823)
    

**2.** Abra proteína no pymol


  **2.1.** Adicione os hidrogênios polares
  
  
  **2.2.** Exporta molécula no formato PDB
  
  ![image](https://github.com/Tutugb/Docking/assets/125391314/928a5bfd-ab69-4f97-8517-8aa097aeefc4)

# Preparo da molécula (ligante)
A molécula a ser preparada nesse caso pode ser um inibidor, fármaco, toxina que conheça a estrutura química em pelo menor formato 2D
**1.** Exportação da molécula do banco de dados

**1.1.** Molécula presente no banco de dados do pubchem
   
**1.1.1.** Molécula com estrutura 3D
      
**1.1.1.1.** Nesse caso só é preciso baixar a molécula no formado SDF do formato 3D
   ![image](https://github.com/Tutugb/Docking/assets/125391314/5fb78c6b-0942-4e60-8773-5fda1eae083f)
   
**1.1.1.2.** Abre arquivo no pymol e faz a conversão para formato pdb
   
   **1.1.2.** Molécula sem estrutura 3D
   
   **1.1.2.1.** Nesse caso deve baixar a molécula no formato SDF, mas no formato 2D e convertê-la para 3D no programa do avogadro e no formato PDB
    
   **1.2.** Molécula não presente no banco de dados do pubchem

Nesse caso há necessidade de pesquisar a molécula em outro banco de dados

* Zinc
```python
https://zinc.docking.org/
```
* Drugbank
```python
https://go.drugbank.com/
```
**2.** Convertendo para o formato PDBqt

Para essa etapa é necessário o software MGLTools onde faz a conversão do formato PDB para PDBqt de forma rápida

**2.1.** Abrir a molécula do formato PDB

![image](https://github.com/Tutugb/Docking/assets/125391314/ed3cd015-bf33-41d7-84e6-d182437334bd)

**2.2.** Exportar no formato PDBqt

![image](https://github.com/Tutugb/Docking/assets/125391314/f63dc7d6-7bd6-4a82-bf78-57e2772292b1)


