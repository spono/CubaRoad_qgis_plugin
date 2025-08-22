# CubaRoad 
## Outil de calcul automatique des volumes de déblai/remblai le long d'un tracé 

Version : 0.1 
Langage : Python 3.x  

Financement : **Office National des Forêts - Pôle RDI de Chambéry** (*laurent.malabeux@onf.fr*)  
![ONF](img/onf_logo.gif?raw=true)

Conception et développement : **Sylvain DUPIRE, SylvaLab - 2021** (*sylvain.dupire@sylvalab.fr*)   
![SylvaLab](img/logo_sylvalab.png?raw=true)

---
### Contexte et objectif de CubaRoad

Les modèles numériques de terrain (MNT) dérivés de données spatiales à haute résolution (LiDAR, radar...) permettent aujourd'hui de représenter très fidèlement le relief. Cette représentation de qualité ouvre la porte à de nombreuses applications numériques pour faciliter le travail de terrain des forestiers, en particulier dans les zones les plus accidentées.

Dans le cadre de la conception de nouvelles dessertes forestières (route ou piste), ce type de MNT permet d'effectuer un calcul automatique de cubature afin d'évaluer les volumes de déblai et remblai.

CubaRoad s'inscrit dans cette logique et ambitionne d'aider les forestiers dans la conception de nouvelles dessertes forestières en leur permettant de calculer automatiquement ces volumes le long d'un tracé. L'outil retourne un tableur récapitulant les informations utiles à la conception de nouvelle desserte pour chaque segment analysé. Il est aussi possible de visualiser le profil en travers théorique de la desserte avant et après la création de la route pour chaque point d'analyse.  

![SylvaLab](img/illustration.png?raw=true)

Tags = ___Desserte___, ___forestière___, ___montagne___, ___cubature___, ___MNT___, ___déblai___, ___remblai___

---  
### Données en entrée de CubaRoad

**Données spatiales obligatoires** :

- Modèle numérique de terrain (raster de préférence issu de données Lidar)
- Tracé (shapefile de ligne) avec pour chaque segment la définition de :
	- Largeur de la plateforme ou largeur d’assise
	- Pente du talus amont
	- Pente du talus aval  
	- Pourcentage de rocher
	- Méthode de calcul 


**Paramètres de modélisation** :
- Pas d'analyse
- Seuil maximal de pente en travers (ripage = 1)
- Seuil minimal de pente en travers (ripage = 0)


### Données en sortie de CubaRoad

- Document rappelant les paramètres de modélisation ainsi que les résultats généraux
- Un tableur avec les résultats par segment
- Tracé reliant les points de niveau (shapefile)
- Tracé reliant les centres de plateformes(shapefile)
- Surface de l'assise de la route (shapefile)
- Surface de l'emprise de la route (shapefile)
- Les points d'analyse (shapefile)
- Un profil pour chaque point d'analyse    
    
![profil](img/profil.png?raw=true)
    
&nbsp;   
  
- - -
**ENGLISH VERSION**

# CubaRoad
## Tool for automatic calculation of cut/fill volumes along a route

### Context and Objective of CubaRoad

Digital elevation models (DEMs) derived from high-resolution spatial data (LiDAR, radar, etc.) now provide a very accurate representation of the terrain. This high-quality representation opens the door to numerous digital applications to facilitate foresters' fieldwork, particularly in the most rugged areas.

When designing new forest access routes (roads or tracks), this type of DEM allows for automatic volume calculations to assess cut and fill volumes.

CubaRoad is part of this approach and aims to assist foresters in the design of new forest access routes by allowing them to automatically calculate these volumes along a route. The tool returns a spreadsheet summarizing the information useful for designing new access routes for each segment analyzed. It is also possible to view the theoretical cross-section of the access route before and after the road is created for each analysis point.

![SylvaLab](img/illustration.png?raw=true)

Tags = ___Desserte___, ___forestry___, ___mountain___, ___cubature___, ___DTM___, ___cut___, ___fill___

---  
### CubaRoad Input Data
**Required Spatial Data**:

- Digital Elevation Model (raster preferably from Lidar data)
	- Line (line shapefile) with the definition of the following for each segment:
	- Platform width or base width
	- Upstream slope
	- Downstream slope
	- Rock percentage
	- Calculation method

**Modeling parameters**:
- Step of analysis
- Maximum cross-slope threshold (slip = 1)
- Minimum cross-slope threshold (slip = 0)

### CubaRoad Output Data

Document summarizing the modeling parameters and general results
A spreadsheet with the results per segment
Line connecting the elevation points (shapefile)
Line connecting the platform centers (shapefile)
Road base area (shapefile)
Road right-of-way area (shapefile)
Analysis points (shapefile)
A profile for each analysis point

![profil](img/profil.png?raw=true)
    
&nbsp; 

---  


__Licence CubaRoad :__

    Copyright (C) 2021 by Sylvain DUPIRE - SylvaLab.

    This program is free software: you can redistribute it and/or modify
    it under the terms of the GNU General Public License as published by
    the Free Software Foundation, either version 3 of the License, or
    (at your option) any later version.

    This program is distributed in the hope that it will be useful,
    but WITHOUT ANY WARRANTY; without even the implied warranty of
    MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
    GNU General Public License for more details.

    You should have received a copy of the GNU General Public License
    along with this program.  If not, see https://www.gnu.org/licenses/



