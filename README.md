# Job Platform AI

Plateforme intelligente de recherche d'emploi et d'assistance aux candidatures.

## Statut
Phase 0 : squelette de développement. Aucun service métier ni collecte réelle n'est implémenté.
Docker, PostgreSQL et le frontend seront configurés dans les étapes suivantes.

## Démarrage sous WSL Ubuntu

```bash
sudo apt update
sudo apt install -y git python3 python3-venv python3-pip curl unzip
python3 -m venv .venv
source .venv/bin/activate
python -m pip install --upgrade pip
python -m pip install -r requirements.txt
[ -f .env ] || cp .env.example .env
chmod 600 .env
python -m pip check
python -m pytest -v
ruff check .
```

Node.js : installer NVM selon https://github.com/nvm-sh/nvm#installing-and-updating puis `nvm install --lts`, `nvm use --lts` et `node --version > .nvmrc`. Aucun paquet npm n'est requis avant le frontend.

## Confidentialité
Ne jamais publier .env, les secrets ni les CV réels. Vérifier `git check-ignore .env .venv/` avant le premier commit.

## Documentation
Voir ROADMAP.md, docs/ et BACKLOG.md.
# platformJob_IA
