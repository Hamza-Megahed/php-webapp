FROM eboraas/apache

RUN apt-get update && apt-get -y install php5 php5-mysql && apt-get clean && rm -rf /var/lib/apt/lists/*
RUN /usr/sbin/a2dismod 'mpm_*' && /usr/sbin/a2enmod mpm_prefork

#exposing port 80 and 443 for SSL/TLS 
EXPOSE 80

CMD ["/usr/sbin/apache2ctl", "-D", "FOREGROUND"]



