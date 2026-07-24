# Start-End Frame Interpolation

Create practical tech animations by interpolating between a start frame and an end frame.

> Live demo: https://rifaterdemsahin.github.io/start-end-frame-interpolation/
> Comparison: https://rifaterdemsahin.github.io/start-end-frame-interpolation/comparison.html
> API reference: https://rifaterdemsahin.github.io/start-end-frame-interpolation/api.html

Example reference: https://youtu.be/ddDJxFnv-qs?t=11

## Start frame

![Start frame](assets/start-frame.png)

## End frame

![End frame](assets/end-frame.png)

## Prompt

Use the start frame and end frame to animate. Make sure the developer types and the
terminal gets more text with colors, and the servers running have lights that change.

## Model selection

Two generation options were considered:

- **Veo 3.1 - Lite** — interpolates between the start and end frames.
- **Omni Flash** — animates from the start frame only.

Veo 3.1 - Lite was selected so the animation could interpolate between both frames.

## Generation

An 8-second video was generated animating between the two frames using Veo 3.1 - Lite,
at a cost of 10 credits.

## Output

<video src="assets/output-animation.mp4" controls width="480"></video>

[Download the output video](assets/output-animation.mp4)

## Comparison

See [comparison.html](comparison.html) for a side-by-side of the generated output against the
[source reference clip](https://youtu.be/ddDJxFnv-qs?t=12).

## API

See [api.html](api.html) for how to trigger the same start/end frame + prompt workflow
programmatically via fal.ai or the Gemini API (Veo), including a snippet builder.

## Cost

See [cost.html](cost.html) for what Google Flow, fal.ai, and the Gemini API charge for this
workflow, plus a calculator for estimating a batch run.
