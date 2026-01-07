# How to Push to Both Repositories

You now have two remotes configured:

1. **origin** → `portfolio-control-systems` (Control Systems Portfolio)
2. **portfolio** → `Portfolio` (Original Data Science Portfolio)

## Push to Both Repositories

After making changes and committing them, you can push to both:

```bash
# Push to control systems portfolio (new)
git push origin main

# Push to original portfolio (data science)
git push portfolio main

# Or push to both at once
git push origin main && git push portfolio main
```

## Push Only to Control Systems Portfolio

```bash
git push origin main
```

## Push Only to Original Portfolio

```bash
git push portfolio main
```

## Check Remote Status

```bash
git remote -v
```

## Note

- The default `git push` will push to `origin` (control-systems portfolio)
- Make sure both repositories are in sync if you want them to have the same content
- Or keep them separate by only pushing relevant changes to each

