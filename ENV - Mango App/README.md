| Service | Build Image Command | Run Container Command |
|---------|---------------------|----------------------|
| EmailAPI | `docker build --secret id=nugetconfig,src="$env:NUGET_CONFIG_PATH" -t mango-email-local:dev .` | `docker run --name mango-emailapi --env-file .env -p 5126:8080 mango-email-local:dev` |
| ShoppingCartAPI | `docker build --secret id=nugetconfig,src="$env:NUGET_CONFIG_PATH" -t mango-shoppingcartapi:local .` | `docker run --name mango-shoppingcartapi --env-file .env -p 5220:8080 mango-shoppingcartapi:local` |
| Web | `docker build -f Frontend/Mango.Web/Dockerfile -t mango-web:local .` | `docker run --name mango-web --env-file Frontend/Mango.Web/.env -p 5048:8080 mango-web:local` |
| CouponAPI | `docker build -t mango-couponapi-local:dev .` | `docker run --name mango-couponapi --env-file .env -p 5104:8080 mango-couponapi-local:dev` |
| OrderAPI | `docker build --secret id=nugetconfig,src="$env:NUGET_CONFIG_PATH" -t mango-orderapi-local:dev .` | `docker run --name mango-orderapi --env-file .env -p 5201:8080 mango-orderapi-local:dev` |
| RewardAPI | `docker build -t mango-rewardapi-local:dev .` | `docker run --name mango-rewardapi --env-file .env -p 5202:8080 mango-rewardapi-local:dev` |
| ProductAPI | `docker build -t mango-productapi-local:dev .` | `docker run --name mango-productapi --env-file ".env" -p 5156:8080 mango-productapi-local:dev` |
| AuthAPI | `docker build --secret id=nuget_config,src="$env:NUGET_CONFIG_PATH" -t mango-authapi-local:dev .` | `docker run --name mango-authapi --env-file .env -p 5005:8080 mango-authapi-local:dev` |
## Services

| Service | Port | Description |
| ------- | ---- | ----------- |
| Mango Auth API | 5005 | Authentication Service |
| Mango Product API | 5156 | Product Management |
| Mango Coupon API | 5104 | Coupon Management |
| Mango Reward API | 5202 | Reward Processing |
| Mango Order API | 5201 | Order Management |
| Mango Shopping Cart API | 5220 | Shopping Cart Service |
| Mango Web | 5048 | Frontend Application |

<img width="1328" height="746" alt="image" src="https://github.com/user-attachments/assets/1e01c7ee-c8e9-4e49-a837-8d6e0c043cdd" />
