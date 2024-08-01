# How to create the patch file
cd libs/community/langchain_community/tools/playwright
git diff --no-prefix --relative=libs/community/langchain_community/tools/playwright/  > playwright_semaphore.patch

# How to apply the patch file
cd .venv/lib/python3.11/site-packages/langchain_community/tools/playwright
patch -p0 < playwright_semaphore.patch