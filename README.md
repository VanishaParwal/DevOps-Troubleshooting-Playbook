# DevOps-Troubleshooting-Playbook

This repository serves as a collection of real-world DevOps and CI/CD troubleshooting case studies. Each case study details a problem encountered, the various diagnostic steps taken, the iterative attempts at resolution, and the ultimate solution.

The goal is to provide a practical guide for common (and uncommon) pipeline failures, security scanning discrepancies, build issues, and deployment challenges. It aims to showcase a methodical debugging approach, practical solutions, and a deep understanding of modern DevOps tooling and principles.

---

## Case Studies

* **[01-Trivy-CrossSpawn-CVE: Resolving a Persistent Security False Positive in CI/CD](01-Trivy-CrossSpawn-CVE/README.md)**
    * **Problem:** Trivy continuously reported a HIGH severity vulnerability (`CVE-2024-21538` in `cross-spawn`) despite local fixes and verified package versions within the Docker image.
    * **Tools/Concepts:** GitHub Actions, Docker, Trivy, `npm`, dependency resolution, `.trivyignore`, false positives, Shift Left.



---

## My Approach to Troubleshooting

My troubleshooting philosophy revolves around a systematic, iterative process:

1.  **Reproduce Locally:** Always attempt to replicate the pipeline failure on my local machine. This is crucial for faster feedback loops ("Shift Left").
2.  **Read Error Messages:** Thoroughly analyze error logs. They often contain explicit clues about the root cause.
3.  **Inspect Environment:** Understand the context – what version of a tool is being used? What's the state of the environment (e.g., Docker layers, `node_modules`, cached files)?
4.  **Isolate Variables:** Change one thing at a time and re-test.
5.  **Verify Assumptions:** Don't just assume a fix worked; *prove* it (e.g., inspecting installed versions inside a container).
6.  **Document & Automate:** Once a solution is found, document the process and, if possible, integrate it into the CI/CD pipeline itself (e.g., `.trivyignore`).


---

Feel free to explore the individual case studies for detailed breakdowns.
