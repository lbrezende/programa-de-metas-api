## Programa De Metas

<img src="https://www.codeship.io/projects/1ec29030-d2fe-0131-5261-7a7c9560a8ff/status"/>

### Requerimentos

1. PHP 5.4
2. Composer https://getcomposer.org/

### Configuração inicial

1. clone this repo
2. install vendor libraries ```composer install```
3. configure database at ```app/config/database.php```
4. run migrations ```php artisan migrate```
5. run seeds ```php artisan db:seed```

### Importação (não finalizada)

Listar os arquivos disponíveis para importação

```
php artisan importer
```

Listar as Worksheets da planilha especificada

```
php artisan importer --filename=decima-primeira-versao-02-04.xls
```

Importar somente as metas

```
php artisan importer:load --filename=decima-primeira-versao-02-04.xls --type=goal
```

Importar projetos de cada tipologia separadamente

```
php artisan importer:load --filename=decima-primeira-versao-02-04.xls --type=project --milestone=1
php artisan importer:load --filename=decima-primeira-versao-02-04.xls --type=project --milestone=2
php artisan importer:load --filename=decima-primeira-versao-02-04.xls --type=project --milestone=3
php artisan importer:load --filename=decima-primeira-versao-02-04.xls --type=project --milestone=4
php artisan importer:load --filename=decima-primeira-versao-02-04.xls --type=project --milestone=5
php artisan importer:load --filename=decima-primeira-versao-02-04.xls --type=project --milestone=6
php artisan importer:load --filename=decima-primeira-versao-02-04.xls --type=project --milestone=7
php artisan importer:load --filename=decima-primeira-versao-02-04.xls --type=project --milestone=8
php artisan importer:load --filename=decima-primeira-versao-02-04.xls --type=project --milestone=9
```

### Testes (forma atual de importação)

Lista de testes implementados e como rodá-los separadamente

```
php artisan behat:run read_xls_file         # read a cell on spreadsheet
php artisan behat:run parse_xls_file        # easily get content from goals and projects
php artisan behat:run validation_xls_file   # validate all data based on some rules
php artisan behat:run importer_xls_file     # import validate data to database
```

### Licença

API Programa de Metas
Copyright (C) 2014 Prefeitura Municipal de São Paulo <http://www.capital.sp.gov.br/>

Este programa é software livre: você pode redistribuí-lo e / ou modificá-
-lo sob os termos da GNU General Public License conforme publicada pela
Free Software Foundation, tanto a versão 3 da licença, ou
(a seu critério) qualquer versão posterior.

Este programa é distribuído na esperança de que ele vai ser útil,
mas SEM QUALQUER GARANTIA; inclusive, sem a garantia implícita de
COMERCIALIZAÇÃO ou de ADEQUAÇÃO A UM DETERMINADO FIM. veja a
GNU General Public License para mais detalhes.

Você deve ter recebido uma cópia da Licença Pública Geral GNU
junto com este programa. Se não, veja <http://www.gnu.org/licenses/>.
