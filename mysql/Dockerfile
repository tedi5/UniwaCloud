# Χρησιμοποίησε την επίσημη εικόνα MySQL ως βάση
FROM mysql:5.7

# Ορισμός των παραμέτρων περιβάλλοντος για το MySQL
ENV MYSQL_ROOT_PASSWORD=rootpassword
ENV MYSQL_DATABASE=mydatabase
ENV MYSQL_USER=myuser
ENV MYSQL_PASSWORD=mypassword

# Αντιγραφή αρχείων παραμετροποίησης (αν χρειάζεται)
COPY my-custom.cnf /etc/mysql/conf.d/

# Προσαρμογή των ρυθμίσεων του MySQL (προαιρετικά)
RUN { command1 && command2 && ... }

# Ανακατασκευή της βάσης δεδομένων (προαιρετικά)
RUN /usr/bin/mysqld_safe --skip-grant-tables & \
    && sleep 5 \
    && mysql -u root -prootpassword -e "CREATE DATABASE mydatabase;"

# Ορισμός του port που θα χρησιμοποιεί το MySQL server
EXPOSE 3306

# Εντολή για την εκκίνηση του MySQL server κατά την εκτέλεση του container
CMD ["mysqld"]