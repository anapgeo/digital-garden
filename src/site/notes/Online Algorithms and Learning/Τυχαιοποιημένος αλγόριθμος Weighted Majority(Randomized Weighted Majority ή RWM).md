---
{"dg-publish":true,"permalink":"/online-algorithms-and-learning/tyxaiopoiimenos-algorithmos-weighted-majority-randomized-weighted-majority-i-rwm/","created":"2025-03-25T14:58:23.182+02:00","updated":"2025-03-25T15:00:15.576+02:00"}
---


![Screenshot_9 1.png](/img/user/Online%20Algorithms%20and%20Learning/Screenshot_9%201.png)

> Σημείωση: Αρχικά ορίζουμε όλες τις δράσεις ισοπίθανες. Στη συνέχεια σε κάθε επανάληψη βρίσκουμε ποιές δράσεις είχαν κόστος 1 και πολλαπλασιάζουμε τα βάρη τους με $\beta$. Έπειτα αθροίζουμε τα νέα βάρη και υπολογίζουμε τις νέες πιθανότητες των ενεργειών ως το κλάσμα του βάρους της κάθε ενέργειας ως προς το συνολικό αθροισμα των βαρών. 



## Ανάλυση Αλγορίθμου 

>Θεώρημα. Έστω $β \in [1/2,1)$. Το κόστος του RWM για οποιαδήποτε ακολουθία, φράσσεται ως εξής: $\mathcal{L}_T\leq \frac{\log_2 N}{1-\beta}+ (2-\beta)\mathcal{L}_T^{\min}$
>
>Eπίσης για $\beta=\max\{1/2, 1-\sqrt{\log (N/T)}\}$, το κόστος φράσεται από: $\mathcal{L}_T\leq\mathcal{L}_T^{\min}+ 2\sqrt{T\log N}$


Απόδειξη

(Η απόδειξη παραλείπετε)


>Παρατήρηση: Το regret γράφεται ώς εξής $R_T\leq 2\sqrt{T\log N}$ συνεπώς για σταθερό αριθμό από experts έχουμε $R_T=O(2\sqrt{T})$ 



