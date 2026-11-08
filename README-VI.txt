HUONG DAN DEPLOY CLOUDFLARE PAGES + D1

1) Tao D1 database trong Cloudflare Dashboard, dat ten tn88web-db.
2) Thay REPLACE_WITH_YOUR_D1_DATABASE_ID trong wrangler.toml bang Database ID that.
3) Chay migration:
   npx wrangler d1 migrations apply tn88web-db --remote
4) Deploy thu muc nay len Cloudflare Pages (Git integration hoac Wrangler Pages).
   Neu dung dashboard Direct Upload, can deploy kem thu muc functions va cau hinh D1 binding:
   Pages > Settings > Functions > D1 database bindings
   Variable name: DB
   Chon database tn88web-db.
5) Deploy lai sau khi gan binding.

Tinh nang:
- Dang ky ten tai khoan, mat khau, so dien thoai khong bat buoc.
- Dang nhap va dang xuat.
- Mat khau duoc bam PBKDF2-SHA256, khong luu mat khau goc.
- Session cookie HttpOnly/Secure, token duoc bam truoc khi luu.
- Khong dung chung tai khoan voi website dich vu khac.

Luu y truoc khi mo cong khai:
- Bat buoc dung HTTPS (Cloudflare Pages cung cap).
- Them rate limiting/chong bot cho API dang ky va dang nhap.
- Them chinh sach bao mat va thong tin lien he.
- Sao luu D1 va kiem tra phuc hoi du lieu.
- Neu khong can so dien thoai, bo truong nay de giam du lieu ca nhan can bao ve.

Khong chua thong tin dang nhap nao cua TN88 hay ben thu ba.
