FROM ubuntu:18.04

RUN apt-get update &&  apt-get install -y --no-install-recommends apache2 libapache2-mod-jk 

ADD conf/apache2/apache2.conf /etc/apache2/apache2.conf

ADD conf/apache2/000-default.conf /etc/apache2/sites-enabled/000-default.conf

ADD conf/jk_mod/workers.properties /etc/libapache2-mod-jk/workers.properties

ADD conf/jk_mod/jk.conf /etc/apache2/mods-available/jk.conf

CMD ["apachectl", "-k", "start", "-DFOREGROUND"]
