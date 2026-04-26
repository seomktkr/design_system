# MegazoneCloud Inspired Design System

[DESIGN.md](./DESIGN.md) extracted from the public [MegazoneCloud](https://www.megazone.com/) website. This is not the official design system. Colors, fonts, and spacing are extracted from the live CSS source (`45b99e30f935daf7.css`, Tailwind CSS v4.1.17 + custom brand tokens).

## Files

| File | Description |
|------|-------------|
| `DESIGN.md` | Complete design system documentation (9 sections + CSS token appendix) |

## Key Design Tokens

| Token | Value |
|-------|-------|
| Primary font | Pretendard (KO) + Noto Sans JP + Noto Sans SC |
| CTA / Link color | `#414aff` (Point Blue) |
| Brand gradient | `linear-gradient(90deg, #32ef7a, #00d7f8 25%, #414aff 50%, #8920ff 75%, #ff41c1)` |
| Body text | `#191919` |
| Background | `#ffffff` / `#f7f7f7` / `#f0f0f0` |
| Border radius | `8px` |

## Usage

Copy `DESIGN.md` to your project root and tell your AI agent:

```
참고 파일: DESIGN.md
MegazoneCloud 디자인 시스템을 기반으로 [페이지명] 페이지를 만들어줘.
```

## Brand Signature

The five-color AI spectrum gradient is MegazoneCloud's most distinctive visual element:

```css
linear-gradient(90deg, #32ef7a, #00d7f8 25%, #414aff 50%, #8920ff 75%, #ff41c1)
```

Use as gradient text on hero headlines for authentic brand feel.
