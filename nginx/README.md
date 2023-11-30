# Nginx Configuration

Sample self-signed Nginx configuration (port 8888) for Jupyter Lab (port 127.0.0.1:8887).

```sh
sudo cp jupyterlab.conf /etc/nginx/conf.d/
```
Generate Jupyter configs.
```sh
jupyter lab --generate-config
```
Modify the Jupyter configurations to allow the reverse proxy.
```toml
# ./.jupyter/jupyter_lab_config.py
c.ServerApp.allow_origin = '*'
c.ServerApp.allow_remote_access = True
```
