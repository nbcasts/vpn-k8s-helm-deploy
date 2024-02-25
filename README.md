# Usage

```
      - name: Deploy
        uses: nbcasts/vpn-k8s-helm-deploy@v1
        with:
          image_label: latest
          github_token: ${{ secrets.GITHUB_TOKEN }}
          kubeconfig: ${{ secrets.KUBECONFIG }}
          kubeconfig_context: the-x-context
          helm_command: helm upgrade my-app-release-name ./my-chart --set "ingress.hosts[0].host=my-cool-url.example.com"
          helm_namespace: my-k8s-namespace
          vpn_wireguard_endpoint: ${{ vars.VPN_WIREGUARD_ENDPOINT }}
          vpn_wireguard_endpoint_public_key: ${{ vars.VPN_WIREGUARD_ENDPOINT_PUBLIC_KEY }}
          vpn_wireguard_ips: ${{ vars.VPN_WIREGUARD_IPS }}
          vpn_wireguard_allowed_ips: ${{ vars.VPN_WIREGUARD_ALLOWED_IPS }}
          vpn_wireguard_private_key: ${{ secrets.VPN_WIREGUARD_PRIVATE_KEY }}
          vpn_wireguard_preshared_key: ${{ secrets.VPN_WIREGUARD_PRESHARED_KEY }}
```
