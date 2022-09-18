# tp_odoo

## Step 1 : Generate a secret yaml file with the following command

      kubectl create secret generic  odoo-pgsql-password --from-literal=odoo=YOUR_PASSWORD -n tp-odoo --dry-run=client -o yaml >tp-odoo-03_secret.yaml

## Step 2 : Apply all manifests

      kubectl apply -f .

## Step 3 : Check that all objects are working

      kubectl -n tp-odoo get all

## Step 4 : Test wordpress

      Open your browser and go to http://YourMasterKubernetesServerIP:31000

## Delete all
kubectl delete -f .

