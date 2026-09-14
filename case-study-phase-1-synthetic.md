cd /path/to/Purview-Data-Governance-Sandbox
cp ~/Downloads/purview-repo-update/README.md .
cp ~/Downloads/purview-repo-update/case-study-phase-1-synthetic.md .
cp ~/Downloads/purview-repo-update/case-study-phase-2-real-cihi-data.md .
git add README.md case-study-phase-1-synthetic.md case-study-phase-2-real-cihi-data.md
git commit -m "Link Phase 1 and Phase 2 case studies; fix broken image paths"
git push
