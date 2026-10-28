### Tianna Zhang

人工智能专业本科生（2027 届），方向是AIGC、计算机视觉、机器学习、具身智能，在钢铁洪流中做人类情感的纽带。
世界上最伟大的不是算法和代码，而是爱。I don't create sight, I breathe meaning into pixels.

Undergraduate majoring in Artificial Intelligence (Class of 2027), focusing on AIGC, computer vision, machine learning and embodied intelligence. I aim to serve as a bond for human emotions amid the surging tide of technology.
The greatest thing in the world is not algorithms and code, but love.
I keep this account small on purpose: a few repos I can defend line by line in an interview, each with tests that run in CI and numbers I measured myself rather than estimated.

## What I'm building

- **[doc-rectify](https://github.com/TiannaZhang925/doc-rectify)** - find a page in a photo and flatten it. The four-point DLT homography solve and the inverse-map bilinear resampler are written on numpy instead of calling `cv2.getPerspectiveTransform` / `cv2.warpPerspective`, so the numerics are visible and testable. 26 unit tests, numpy-only geometry tests run in a separate CI job, and a synthetic ground-truth benchmark that reports corner error as a *signed* offset - which is how I found that my residual was a deterministic 1.5 px dilation bias, plus a benchmark artifact I had written into my own scene generator.
- **[trendai-marketing](https://github.com/TiannaZhang925/trendai-marketing)** - a Qoder CLI Skill that turns an agent into a social-content operator: trend research, per-platform copy generation, image generation, and a four-dimension scoring rubric. Kept public as a brand-neutral template; the brand profile it writes is a placeholder file.

## How I work

- If a library call hides the thing I'm supposed to understand, I implement it and then measure my version against the library's.
- Every number in a README is reproducible by one command in the repo, and I write down what the measurement does *not* cover.
- Failures are designed for: the detection pipeline degrades to a documented fallback instead of throwing, and returns the score breakdown that caused its decision.
- I'd rather ship one correct 300-line module than a framework.

## Next

1. Sub-pixel edge fitting (or anisotropic closing) to remove the dilation bias without losing contour closure under steep perspective.
2. A learned corner head (DIPIM / DTMM style) behind the same `QuadHypothesis` interface, so the classical path stays as the baseline it has to beat.
3. Curved-page unwarping - a 3x3 matrix is the wrong model for a book spine.

Reachable at the email on my profile. Chinese / English both fine.

<!-- Optional: uncomment the community stats cards once you are happy with the repo history.
![stats](https://github-readme-stats.vercel.app/api?username=TiannaZhang925&show_icons=true&hide_rank=true)
-->
