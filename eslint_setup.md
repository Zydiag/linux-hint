
### hyprland workspaces 
- instead of wlr/workspaces use hyprland/workspaces

### ESlint Install
install the following

```bash
sudo npm install --globally eslint-config-standard eslint  eslint-plugin-tailwindcss eslint-config-prettier
```

- install prettier extension 
```bash
npm install --save-dev --save-exact prettier
```

```json
{
  "eslintConfig": {
    "extends": [
      "standard",
      "plugin:tailwindcss/recommended"
    ]
  }
}
``` 



