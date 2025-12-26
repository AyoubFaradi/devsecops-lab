# DevSecOps Lab — CI/CD Security Pipeline

![CI/CD](https://img.shields.io/badge/CI%2FCD-GitHub%20Actions-blue)
![Security](https://img.shields.io/badge/Security-DevSecOps-red)
![Docker](https://img.shields.io/badge/Docker-Enabled-blue)

---

## Description

Ce projet est un **laboratoire DevSecOps** qui démontre l’intégration automatique de la sécurité dans un pipeline **CI/CD GitHub Actions** pour une API **Python Flask** conteneurisée avec **Docker**.

La sécurité est testée **à chaque push** grâce à des outils automatisés.

---

## Architecture du projet

```bash
devsecops-lab/
├── api/
│   └── app.py
├── Dockerfile
├── requirements.txt
└── .github/
    └── workflows/
        └── devsecops.yml
```

<img width="366" height="218" alt="image" src="https://github.com/user-attachments/assets/2361776c-2303-4d95-afad-0173c90d3bad" />

---

## Technologies utilisées

* GitHub Actions (CI/CD)
* Python + Flask
* Docker
* CodeQL (SAST)
* Bandit (Sécurité Python)
* Trivy (Scan image Docker)
* Safety (Sécurité des dépendances)

---

## Pipeline GitHub Actions

<img width="1919" height="864" alt="image" src="https://github.com/user-attachments/assets/5c6391a3-cf6e-429e-af4c-af3852f3e67e" />

---

## Résultats CodeQL

<img width="1903" height="864" alt="image" src="https://github.com/user-attachments/assets/87d17d7b-78fd-425b-b181-c2112c35d248" />

---

## Pipeline après correction

<img width="1902" height="867" alt="Screenshot 2025-12-26 161301" src="https://github.com/user-attachments/assets/08d96f7a-10fa-4801-88bc-7fe6ad4d12af" />

---

# Dependency Security Pipeline
---

## Objectif du projet

Ce projet implémente le principe **DevSecOps** en sécurisant la **supply chain logicielle** via l’analyse automatique des dépendances Python dans un pipeline CI/CD GitHub Actions.
---

### 🔹 requirements.txt

<img width="1551" height="727" alt="image" src="https://github.com/user-attachments/assets/c178f93f-d00f-43b9-aa01-4c60c7d838f5" />

---

### 🔹 Modification du pipeline GitHub Actions

<img width="1887" height="810" alt="image" src="https://github.com/user-attachments/assets/eec99bf4-74ef-4305-8605-9a13bf316bca" />

---

### 🔹 Push du code

```bash
git pull --rebase origin main
git add .
git commit -m "Add secure Python dependencies"
git push origin main
```

<img width="1554" height="350" alt="image" src="https://github.com/user-attachments/assets/6b93fb2a-2daa-40f4-bac7-d549ac1f022f" />

---

## GitHub → Actions → DevSecOps Pipeline

<img width="1902" height="862" alt="Screenshot 2025-12-26 161812" src="https://github.com/user-attachments/assets/ccf2bd42-5fab-4f6e-a9f8-3fe5781d9cff" />

* Sécurisation complète de la chaîne d’approvisionnement logicielle  
* Pipeline CI/CD DevSecOps entièrement automatisé et conforme aux bonnes pratiques

---

## Conclusion

L’approche **DevSecOps** a permis d’intégrer la sécurité de la supply chain directement dans le pipeline CI/CD.

Grâce au scan automatique des dépendances avec **Safety**, toute bibliothèque vulnérable est détectée et bloque le pipeline avant le build Docker, garantissant ainsi une application plus **sécurisée**, **fiable** et **conforme**.

