        private async void theWebView_NavigationCompleted(WebView sender, WebViewNavigationCompletedEventArgs args)
        {
            string returnStr = await theWebView.InvokeScriptAsync("eval", new string[] { SetBodyOverFlowHiddenString });
        }

 
        string SetBodyOverFlowHiddenString = @"function SetBodyOverFlowHidden()
        {
            document.body.style.overflow = 'hidden';
            return 'Set Style to hidden';
        } 
        // now call the function!
        SetBodyOverFlowHidden();";
