# 1. INTRODUCTION

- [x] Welcome
- [x] Requirements
- [x] Library vs Framework
- [x] Old vs New Version
- [x] Project Setup

<br>

---

<br>

## ✅ Next.js 초기 설정

#### 1️⃣ 프로젝트 초기화

```bash
npm init -y
```

<br>

#### 2️⃣ package.json 파일 수정

- `license` 변경

  ```json
  {
    "license": "MIT" // ISC → MIT 변경
  }
  ```

<br>

#### 3️⃣ `react`, `next`, `react-dom` 설치

```bash
npm install react@latest next@latest react-dom@latest
```

<br>

#### 4️⃣ package.json 파일 수정

- `scripts` 명령어 등록

  ```json
  {
    "scripts": {
      "dev": "next dev"
    }
  }
  ```

<br>

#### 5️⃣ `page.tsx`, `layout.tsx` 파일 생성

> next.js에서 해당 파일이 없으면 자동으로 생성해준다.
>
> 이를 root segment라고 한다.

<br>

- `app/pages.tsx` or `app/pages.jsx` 파일 생성
- `app/page.tsx`
  ```tsx
  export default function Page() {
    return <h1>Hello Next.js</h1>;
  }
  ```
- `app/layout.tsx`

  ```tsx
  export const metadata = {
    title: "Next.js",
    description: "Generated by Next.js",
  };

  export default function RootLayout({
    children,
  }: {
    children: React.ReactNode;
  }) {
    return (
      <html lang='en'>
        <body>{children}</body>
      </html>
    );
  }
  ```
