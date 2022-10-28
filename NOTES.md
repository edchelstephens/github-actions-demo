# Environment variables and secrets

```

steps:
    - name: Hello World

```

## 2 Ways to pass a secret in workflow
1. As an input using:

```
steps:
    - name: Hello World
        with:
            super_secret_input: ${{ secrets.MySecret }}
```

2. As an environment variable using:
```
steps:
    - name: Hello World
        env:
            super_secret_input: ${{ secrets.MySecret }}
```
