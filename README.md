# magento2-docker
Magento2 automated docker installation

# Checklist
- Ensure you have composer installed and available in your local path
If you do not have composer installed, refer to https://getcomposer.org/download/ to install composer

- Ensure you have an up and running installation of docker, if not refer to
https://docs.docker.com/get-started/

# Setup

### Automated Setup (New Project)

Run this automated one-liner from the directory you want to install your project.

```bash
curl -s https://raw.githubusercontent.com/KiprotichMaritim/magento2-docker/master/lib/onelinesetup | bash -s -- magento2.test 2.3.5-p1
```

### Composer Authentication

First setup Magento Marketplace authentication (details in the [DevDocs](http://devdocs.magento.com/guides/v2.0/install-gde/prereq/connect-auth.html)).

Copy `src/auth.json.sample` to `src/auth.json`. Then, update the username and password values with your Magento public and private keys, respectively. Finally, copy the file to the container by running `bin/copytocontainer auth.json`.

### Redis

Redis is now the default cache and session storage engine, and is automatically configured & enabled when running `bin/setup` on new installs.

## Credits

### Mark Shust

Certified Magento Developer & Architect
