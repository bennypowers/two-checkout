# \<two-checkout\>

Polymer Wrapper for 2Checkouts payments

## Usage
<!--
```
<custom-element-demo>
  <template>
    <link rel="import" href="../paper-input/paper-input.html">
    <link rel="import" href="../paper-button/paper-button.html">
    <link rel="import" href="../show-json/show-json.html">
    <link rel="import" href="two-checkout.html">
    <template is="dom-bind">
      <div>
        <next-code-block></next-code-block>
      </div>
    </template>
  </template>
</custom-element-demo>
```
-->
```html
<paper-input label="Publishable Key" value="{{publishableKey}}"></paper-input>
<paper-input label="Seller Id" value="{{sellerId}}"></paper-input>
<paper-input label="Credit Card Number" value="{{ccNo}}"></paper-input>
🔓 Use <a href="https://www.2checkout.com/documentation/sandbox/test-data">Test Numbers</a> Only!
<section class="row">
  <paper-input label="MM" value="{{expMonth}}"></paper-input>
  <paper-input label="YY" value="{{expYear}}"></paper-input>
  <paper-input label="CVV" value="{{cvv}}"></paper-input>
</section>

<paper-button onclick="submit()">Submit</paper-button>

<two-checkout id="tco"
    sandbox
    publishable-key="[[publishableKey]]"
    seller-id="[[sellerId]]"
    cc-no="[[ccNo]]"
    exp-month="[[expMonth]]"
    exp-year="[[expYear]]"
    cvv="[[cvv]]"
    token="{{token}}"
    response="{{response}}"
    error="{{error}}"
></two-checkout>

<span>[[error]]</span>

<show-json hide-copy-button json="[[response]]"></show-json>

<script>
  const submit = () => tco.requestToken();
</script>
```
