<!-- LOVABLE:BEGIN -->
> [!IMPORTANT]
> This project is connected to [Lovable](https://lovable.dev). Avoid rewriting
> published git history — force pushing, or rebasing/amending/squashing commits
> that are already pushed — as it rewrites history on Lovable's side and the
> user will likely lose their project history.
>
> Commits you push to the connected branch sync back to Lovable and show up in
> the editor, so keep the branch in a working state.
<!-- LOVABLE:END -->

- Data access: client pages query the database directly with the browser client (RLS enforced); privileged admin actions go through SECURITY DEFINER RPCs that check has_role. Why: keeps rules in the database.
- Matching logic lives in src/lib/matching.ts (pure, tested). Why: verifiable scoring, no random scores.
- Profile email column is not granted to clients; only admin_list_users exposes it. Why: privacy.
