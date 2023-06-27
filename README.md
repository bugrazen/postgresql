![elephant](https://github.com/bugrazen/postgresql/assets/95212909/09575a66-8246-4ce5-bcc5-a534ee1cb55b)

---

# Ubuntu Server için PostgreSQL kurulum adımları
## 1. Dosya deposu yapılandırmasını oluşturun:
```
sudo sh -c 'echo "deb http://apt.postgresql.org/pub/repos/apt $(lsb_release -cs)-pgdg main" > /etc/apt/sources.list.d/pgdg.list'
```

## 2. Depo imzalama anahtarını içe aktarın:
```
wget --quiet -O - https://www.postgresql.org/media/keys/ACCC4CF8.asc | sudo apt-key add -
```

## 3. Paket listelerini güncelleyin:
```
sudo apt-get update
```

## 4. PostgreSQL'in en son sürümünü yükleyin.
### Belirli bir sürüm istiyorsanız, 'postgresql' yerine 'postgresql-14' veya benzerini kullanın:
```
sudo apt-get -y install postgresql
```

## 5. kurduğumuz PostgreSQL' in durumunu sorgulamak için:
```
sudo systemctl status postgresql
```

## 6. PostGIS eklentisi kurulumu:
```
sudo apt install postgis
```

---

# Kurulum sonrası işlemler

## PostgreSQL veritabanı sunucusuna "postgres" kullanıcısıyla giriş yapmak için:
```
sudo -u postgres psql
```
