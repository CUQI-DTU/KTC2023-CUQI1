# EIT Image Reconstruction Algorithm

This repository contains the code and documentation for our submission to the [Kuopio Tomography Challenge 2023](https://www.fips.fi/KTC2023.php).

Electrical Impedance Tomography (EIT) Reconstruction Competition. In this competition, we present our approach to reconstruct high-quality images from EIT measurements.

Electrical Impedance Tomography (EIT) is a powerful technique for non-invasively imaging the electrical conductivity distribution within objects. Our submission focuses on developing an innovative algorithm that enhances the quality and accuracy of EIT image reconstructions.

## Authors
- Amal Mohammed A Alghamdi (DTU), Denmark
- Martin Sæbye Carøe (DTU), Denmark
- Jasper Marijn Everink (DTU), Denmark
- Jakob Sauer Jørgensen (DTU), Denmark
- Kim Knudsen (DTU), Denmark
- Jakob Tore Kammeyer Nielsen (DTU), Denmark
- Aksel Kaastrup Rasmussen (DTU), Denmark
- Rasmus Kleist Hørlyck Sørensen (DTU), Denmark
- Chao Zhang (DTU), Denmark

## Addresses
DTU: Technical University of Denmark, Department of Applied Mathematics and Computer Science Richard Petersens Plads Building 324 2800 Kgs. Lyngby Denmark

## Description of the algorithm

We have used the provided code for the EIT image reconstruction with the following modifications:
- Additional Tikhonov regularization has been added to penalize close to the missing electrodes.
- The Otsu segmentation algorithm has been replaced by the Chan-Vese segmentation algorithm from scikit-image.

## Installation instructions
To run our EIT image reconstruction algorithm, you will need:

- Python 3.x
- Required Python libraries (listed in `requirements.txt`)
- Access to the provided dataset (not included in this repository)

## Usage instructions

```
python main.py path/to/input/files path/to/output/files difficulty
```

## Examples
|   	|  Ref	| Level 1 	| Level 4 	| Level 7 	|
|----------	|-----	|---	|---	|---	|
|   **ta**	| ![](results/01.png)	| ![](results/11.png)	|  ![](results/41.png) 	|   ![](results/71.png)	|   
|   **tb**	| ![](results/02.png)	| ![](results/12.png)	|  ![](results/42.png) 	|   ![](results/72.png)	|
|   **tc**	| ![](results/03.png)	| ![](results/13.png)	|  ![](results/43.png) 	|   ![](results/73.png)	|
|   **td**	| ![](results/04.png)	| ![](results/14.png)	|  ![](results/44.png) 	|   ![](results/74.png)	|  

Scores for each sample and angle:

|   	|  Ref	| Level 1 	| Level 4 	| Level 7 	|
|-----	|---	|---	|---	|
|**ta**	|0.988	|0.963	|0.916|
|**tb** |0.933	|0.892	|0.785|
|**tc**	|0.956	|0.918|	0.830|
|**td**	|0.967	|0.960|	0.940|

{.include}
results/scores.md

## Repository content

## License
