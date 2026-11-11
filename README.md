# Algebra Lineare e Programmazione Lineare

Metodi numerici di base per l'ottimizzazione: decomposizione ai valori singolari, minimi quadrati e programmazione lineare vincolata.

## Contenuto — [`algebra_e_programmazione_lineare.ipynb`](algebra_e_programmazione_lineare.ipynb)

* Decomposizione ai valori singolari (**SVD**, $A = U \Sigma V^T$): verifica della ricostruzione e numero di condizionamento.
* **Minimi quadrati** su dati rumorosi tramite pseudo-inversa $x = V \Sigma^{-1} U^T b$, confrontati con `np.linalg.lstsq`.
* **Programmazione lineare** con `scipy.optimize.linprog` (algoritmo HiGHS): massimizzazione di $Z = 3x_0 + 5x_1$ con i vincoli $x_0 + 2x_1 \le 8$ e $4x_0 + 2x_1 \le 16$.
* Rappresentazione grafica della **regione ammissibile**, della retta di isoprofitto e del punto di ottimo.

## Risultati

* Retta stimata: intercetta 1.1289 e pendenza 2.3840 (valori veri 1.0 e 2.5); la soluzione via SVD coincide con `lstsq` e il numero di condizionamento è 11.69.
* Ottimo della programmazione lineare in $(x_0, x_1) = (8/3, 8/3)$ con $Z = 64/3 \approx 21.33$, nel vertice in cui si incontrano i due vincoli.

## ▶️ Esecuzione

Serve Python 3.9 o successivo.

```bash
git clone https://github.com/lancellottimatteo19/linear-algebra-linear-programming.git
cd linear-algebra-linear-programming
pip install -r requirements.txt
jupyter lab
```

I notebook sono salvati con gli output, quindi grafici e risultati si vedono anche direttamente su GitHub.
