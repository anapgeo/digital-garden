---
{"dg-publish":true,"permalink":"/content/algorithmos-exponential-weighted-average/","created":"2025-03-25T14:58:23.119+02:00","updated":"2025-03-25T14:59:33.543+02:00"}
---

![Screenshot_8 2.png](/img/user/content/Screenshot_8%202.png)


## Ανάλυση και σχόλια

> Θεώρημα. Έστω μια συνάρτηση απώλειας που είναι κυρτή (στο πρώτο όρισμα), με πεδίο τιμών στο $[0,1]$ Τότε για κάθε παράμετρο $η>0$ και για κάθε ακολουθία $y_1,...,y_T\in \mathcal{Y}$, το regret του ExponentialWeightedAverage ύστερα από T γύρους φράσσεται ως εξής:
> 
> - $R_T\leq \frac{\log N}{η} + \frac{ηT}{8}$
> - για $η=\sqrt{8\log N/T}$, το regret φράσσεται από: $R_T\leq \sqrt{(T/2)\log N}$



