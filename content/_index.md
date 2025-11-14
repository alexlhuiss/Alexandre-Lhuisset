---
# Leave the homepage title empty to use the site title
title: ''
date: 2022-10-24
type: landing

design:
  # Default section spacing
  spacing: '6rem'

sections:
  - block: resume-biography-3
    content:
      # Choose a user profile to display (a folder name within `content/authors/`)
      username: admin
      text: ''
      # Show a call-to-action button under your biography? (optional)
      button:
        text: Full CV
        url: uploads/resume.pdf
      headings:
        about: ''
        education: ''
        interests: ''
      design:
        css: |
          .profile {
            margin-bottom: 2rem;        /* espace sous la photo */
          }
          .portrait-title h1 {
            margin-top: 1rem;           /* espace entre le nom et la prononciation */
            margin-bottom: 1rem;        /* espace entre le nom et le titre */
          }
          .portrait-title .big-title {
            margin-bottom: 1.5rem;      /* espace sous ton titre */
          }
          .portrait-title + .btn-download {
            margin-top: 2rem;           /* espace au dessus du bouton CV */
          }
    design:
      background:
        image:
          filename: stacked-peaks.svg
      spacing:
        # top, right, bottom, left
        padding: ['0', '80px', '0', '0']
  - block: markdown
    content:
      title: 'Collaborate'
      subtitle: ''
      text: |-
        Do not hesitate to reach out in order to collaborate
    design:
      columns: '1'
  - block: collection
    id: papers
    content:
      title: Featured Publication
      filters:
        folders:
          - publications
        featured_only: true
    design:
      view: article-grid
      columns: 1
  - block: collection
    content:
      title: Recent Publications
      text: ''
      filters:
        folders:
          - publications
        exclude_featured: false
    design:
      view: citation
---
