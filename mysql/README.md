# Εικονικό Εργαστήριο MySQL

Αυτό το εικονικό εργαστήριο περιέχει δύο containers Docker για τη δημιουργία ενός μητρώου MySQL και ενός MySQL slave για αντίγραφα ασφαλείας.

## Οδηγίες Εγκατάστασης

Για να εγκαταστήσετε και να τρέξετε το εικονικό εργαστήριο, ακολουθήστε τα παρακάτω βήματα:

1. Κλωνοποιήστε το αποθετήριο από το GitHub:

   ```bash
   git clone https://https://github.com/tedi5/UniwaCloud
   cd mysql-replication-vlab



Ξεκινήστε τα containers χρησιμοποιώντας το Docker Compose:

docker-compose up -d

Για να συνδεθείτε στα containers του MySQL με τον MySQL client:

# Σύνδεση στον MySQL Master
docker exec -it mysql-master mysql -u root -prootpassword

# Σύνδεση στον MySQL Slave
docker exec -it mysql-slave mysql -u root -prootpassword


H

#Αν αυτο δεν πατυχει μπειτε απο εδω
mysql -u root -p


Για να ελέγξετε την κατάσταση αναγωγής του MySQL slave:

docker exec -it mysql-slave mysql -u root -prootpassword -e "SHOW SLAVE STATUS\G;"

Η ΜΕΤΑ ΤΟ mysql -u root -p

SHOW SLAVE STATUS;
SHOW MASTER STATUS;
