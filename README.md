# Coolify Build Secrets Test

## How to use

1. Create a new resource in Coolify with this repository
2. Set **Build Pack** to "Docker Compose" and set base directory to `/apps/[select-test-app-directory]`
3. Add a new environment variable named `TEST_SECRET` with any value. Don't check **Build Variable?**.
4. Deploy
5. Go to **Command** and run `cat test_secret_file` command
6. Command output should be whatever value you set to `TEST_SECRET`

You might need to run `docker compose build --no-cache` after changing the value
to update it in the container.

For additional info and research, see [Docker build secrets in Coolify](https://github.com/Cryszon/me/blob/main/tools/coolify/docker-build-secrets-in-coolify.md).
