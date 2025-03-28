---
{"dg-publish":true,"permalink":"/online-algorithms-and-learning/algorithmos-halving-alanthastos-expert/","created":"2025-03-25T14:58:23.067+02:00","updated":"2025-03-28T12:39:04.343+02:00"}
---



Ας θεωρήσουμε $\mathcal{Y}=\{0,1\}$ και $L(\hat{y},y)=|\hat{y}-y|$(δηλαδή classification πρόβλημα). Επίσης θεωρούμε πως υπάρχει κάποιος αλάνθαστος expert (δεν ξέρουμε ποιος).

Μοντέλο Φράγματος Σφαλμάτων (Mistake Bound model):

-  Πόσα λάθη χρειάζονται για να μάθουμε μια έννοια (τον τέλειο expert);
-  Μόλις ανακαλύψουμε τον σωστό expert (concept) δεν θα ξανακάνουμε λάθη στο μέλλον
-  ο μέγιστος αριθμός λαθών για μια συγκεκριμένη έννοια: $M_{ALG}(c)=\max_{x_1,\dots,x_T} |mistakes(ALG,c)|$
- Για μια κλάση εννοιών $C$ έχουμε $M_{ALG}(C)=\max_{c\in C} M_{ALG}(c)$
- Ψάχνουμε να βρούμε αλγορίθμους που ελαχιστοποιούν το $M_{ALG}(C)$


### Ο αλγόριθμος 

![Screenshot_7 1.png|500](/img/user/Online%20Algorithms%20and%20Learning/Screenshot_7%201.png)


> Σημείωση: Πρακτικά για κάθε γύρο προβλέψεων λαμβάνουμε τα δεδομένα $x_t$. Στη συνέχεια κάνουμε μια πρόβλεψη με βάση το majority vote από τις συμβουλές $H_t$ των experts που "εμπιστευόμαστε". Αρχικά περιλαμβάνονται σε αυτούς όλοι οι διαθέσιμοι experts. Στη συνέχεια, μετά από κάθε πρόβλεψη, αν η πρόβλεψη που κάναμε ήταν λάθος τότε αφαιρούμε όσους experts έκανα λάθος πρόβλεψη(οι οποίοι λόγω του majority vote θα είναι τουλάχιστον οι μισοί)

Πόσα σφάλματα απαιτούνται για την εύρεση του αλάνθαστου expert;

> Θεώρημα: Έστω $H$ ένα πεπερασμένο σύνολο υποθέσεων(experts). Τότε: $M_{halving}(H)\leq \log_2|H|$


Απόδειξη

Ο αλγόριθμος προβλέπει χρησιμοποιώντας πλειοψηφική ψήφο από τους εναπομείναντες experts (υποθέσεις). Άρα κάθε φορά που η πρόβλεψη είναι λανθασμένη, αφαιρούνται τουλάχιστον οι μισοί experts. Αρα μετά από $\log_2 |H|$ σφάλματα έχει μείνει μόνο μία υπόθεση(expert) η οποία θα είναι η αλάνθαστη
