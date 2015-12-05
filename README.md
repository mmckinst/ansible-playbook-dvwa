[![Travis](https://img.shields.io/travis/mmckinst/ansible-playbook-dvwa.svg)](https://travis-ci.org/mmckinst/ansible-playbook-dvwa)

Instructions
---
This is the ansilbe playbook used to build
https://atlas.hashicorp.com/mmckinst/boxes/dvwa . If you downloaded the box from
hashicorp, you'll want to forward guest port 80 to host port 8080 with
`config.vm.network "forwarded_port", guest: 80, host: 8080` and you can access
everything at http://127.0.0.1:8080 . For the reCAPTCHA bypass to work, you'll
need to get keys from [reCAPTCHA](https://www.google.com/recaptcha/admin/create)
and edit `/var/www/html/config/config.inc.php`

If you want to build the box yourself:

1. add values for `recaptcha_public` and `recaptcha_private` to vars.yml from [reCAPTCHA](https://www.google.com/recaptcha/admin/create)
2. vagrant up
3. visit http://127.0.0.1:8080/setup.php

License
---
```
Copyright 2015 Mark McKinstry

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```
