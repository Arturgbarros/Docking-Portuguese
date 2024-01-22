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
   ![image](https://github.com/Tutugb/Docking/assets/125391314/b6cf63b9-8ed7-4c28-b1be-6295a2106e2b)

****2**.** Abra proteína no pymol

**2.1.** Retire as águas
   
![image](https://github.com/Tutugb/Docking/assets/125391314/3694eb9e-b237-4190-a4d7-4f8e25a35d37)

   **2.2.** Adicione os hidrogênios polares
   
![image](https://github.com/Tutugb/Docking/assets/125391314/a30cf557-d677-4b9a-98db-90620cbd1b26)

   **2.3.** Exporta a molécula como formato PDB

   ![image](https://github.com/Tutugb/Docking/assets/125391314/ae50641c-c7e4-4c0f-ae24-9435d4103311)

## Proteína extraida do Uniprot
**1.**  Verifica a existência da estrutura por homologia no banco de dados do Uniprot para importar uma estrutura com confiabilidade relativa, procurando pelo nome da proteína ou o seu gene promotor.


**1.1.** Caso encontre baixe no formato disponível

![image](https://github.com/Tutugb/Docking/assets/125391314/a72ab6c7-0ef7-4081-ba4e-6956900fa823)
    

**2.** Abra proteína no pymol


  **2.1.** Adicione os hidrogênios polares
  
  
  **2.2.** Exporta molécula no formato PDB
  
  ![image](https://github.com/Tutugb/Docking/assets/125391314/928a5bfd-ab69-4f97-8517-8aa097aeefc4)

## Preparo da proteína no MGLTools
#### Leitura da proteína
![image](https://github.com/Tutugb/Docking/assets/125391314/f466ede9-a67c-417e-8cd3-0ea550ac181e)
### Checagem e reparo de átomos faltantes
###### Checagem
![image](https://github.com/Tutugb/Docking/assets/125391314/2cd49321-e512-4a87-851c-0bf260bb45df)

Devem ser selecionados todos os átomos faltantes para que sejam reparados

![image](https://github.com/Tutugb/Docking/assets/125391314/5b5e11b5-a26e-4dc9-9106-e03a87db04de)

###### Reparo 
![image](https://github.com/Tutugb/Docking/assets/125391314/2c29d931-772c-4338-9b89-9183671b5c7f)

**OBS:** Após o reparo refaça a checagem para ter certeza que todos os átomos foram incluídos 

### Adicionar carga de kolman 
![image](https://github.com/Tutugb/Docking/assets/125391314/cab1b4c4-7b32-4781-a86a-2d083bdf98ab)
### Preparo da GridBox para blinding docking
#### Adicionando gridbox
![image](https://github.com/Tutugb/Docking/assets/125391314/dd7bfe8d-c202-458b-8904-08279e57297c)
#### Englobanco toda proteína com a gridbox
Para arrumar gridbox envolta da proteína só é preciso ajeitar os parâmetros em "grid options" onde fará o ajuste para a localização da grid e o tamanho
![image](https://github.com/Tutugb/Docking/assets/125391314/4283d061-5012-449d-a515-4f7e6252fdb6)

Quando a protéina estiver toda envolta pela gridbox como abaixo é preciso salvar cada uma das partes
![image](https://github.com/Tutugb/Docking/assets/125391314/4286809c-a7a8-4960-8bc1-161ca470c532)
**OBS:** Em casos onde a proteína é muito grande e uma grid box não engloba toda a proteína para o blinding docking é necessário preparar várias gridboxs onde cada uma engloba uma parte da proteína porém com todas tendo uma parte com intersecção para ter certeza que não faltou nenhuma parte da proteína a se englobar para o teste de docking molecular
#### Salvando partes
##### Salvando posição e forma da gridbox
![image](https://github.com/Tutugb/Docking/assets/125391314/d1da240e-239b-440b-8175-c0739a74630d)
##### Escolhendo local onde os arquivos serão salvos localmente
![image](https://github.com/Tutugb/Docking/assets/125391314/c13995fe-6a51-44c7-86bd-c7a1094b8801)
Qualquer escrita na opção "Startup directory" deve ser exluida e depois clicar em "set" e em seguida "browse" para que assim seja possível escolher o local onde deseja salvar os seus arquivos
![image](https://github.com/Tutugb/Docking/assets/125391314/288f9079-e68a-4e81-b5f0-839673dce7c4)
#### Salvando arquivo da gridbox

![image](https://github.com/Tutugb/Docking/assets/125391314/c9305e1b-b753-4910-8423-a7929c821189)

Na aba a qual é aberta logo em seguida nas opções "receptor", "ligand" e "out" é necessário colocar duas letras independe de quais letras sejam

![image](https://github.com/Tutugb/Docking/assets/125391314/1dbe27f0-8af0-4173-a82c-0263c41e0ff8)

**OBS:** O arquivo será salvo como "config", porém é necessário modificá-lo para o mesmo no o qual vai salvar o arquivo da proteína no formato PDBqt para que não ocorra conflito no momento do processo de docking molecular 
#### Salvando proteína em PDBqt
![image](https://github.com/Tutugb/Docking/assets/125391314/8705bf73-9ca1-47c1-9f4e-1f639705d278)

Deve ser selecionada a molécula que deseja exportar e essa é a proteína onde é necessário clicar no elemento do nome da proteína e em seguida em "select molecule"

![image](https://github.com/Tutugb/Docking/assets/125391314/dfff6774-ab62-4b83-bf9b-f26ebe8df588)

**OBS1:** Em alguns casos aparecem avisos sobre a questão estrutural da proteína esses só precisam ser aceitos onde não causarão nenhum resultado enviezado nos resultados
**OBS2:** Salve a proteína no formato PDBqt com um nome sem nenhum caracter especial nem espaço e assim nomeie o arquivo da gridbox igual ao arquivo da proteína no formato PDBqt 

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

# Docking
